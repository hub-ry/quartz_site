  ---                                                                                                                                                                                                                                                              
  What was built                                                                                                                                                                                                                                                   
                                                                                                                                                                                                                                                                   
  Project structure                                                                                                                                                                                                                                                
                                                                                                                                                                                                                                                                   
  cordas/                                                                                                                                                                                                                                                          
  ├── .env.example                          ← env var template                                                                                                                                                                                                     
  ├── lib/                                                                                                                                                                                                                                                         
  │   ├── supabase.ts                       ← Supabase client + full DB types
  │   └── spotify.ts                        ← PKCE OAuth, token refresh, currently-playing fetch
  ├── context/
  │   └── auth.tsx                          ← AuthProvider (session, profile, signIn/Up/Out, Spotify tokens)
  ├── hooks/
  │   └── use-push-token.ts                 ← Registers device + saves Expo push token to profile
  ├── app/
  │   ├── _layout.tsx                       ← Root layout: AuthProvider + auth-redirect guard
  │   ├── (auth)/
  │   │   ├── _layout.tsx
  │   │   ├── sign-in.tsx                   ← Email/password auth, @purdue.edu gated
  │   │   └── connect-spotify.tsx           ← Spotify PKCE OAuth screen
  │   └── (tabs)/
  │       ├── _layout.tsx                   ← 4 tabs: Home, Matches, Charts, Profile
  │       ├── index.tsx                     ← Home feed (live co-listen events)
  │       ├── matches.tsx                   ← Personal match history
  │       ├── leaderboard.tsx               ← Campus charts (queries track_leaderboard view)
  │       └── profile.tsx                  ← Display name, avatar, linked social picker
  ├── supabase/
  │   ├── migrations/001_init.sql           ← Full schema: profiles, currently_playing, co_listens, leaderboard view
  │   └── functions/match-listeners/
  │       └── index.ts                      ← Edge Function: polls Spotify → finds pairs → inserts co_listens → push notifs
  └── constants/theme.ts                    ← Updated tint to Cordas violet #7C3AED

  Auth flow

  No session  →  /(auth)/sign-in
  Session, no Spotify token  →  /(auth)/connect-spotify
  Session + Spotify token  →  /(tabs)

  To get running

  1. Copy env file: cp .env.example .env and fill in your keys
  2. Supabase: create a project, run supabase/migrations/001_init.sql, then wire enforce_purdue_email to the "Before user is created" auth hook in the Dashboard
  3. Spotify: create an app at developer.spotify.com, add redirect URI cordas://spotify-auth
  4. Edge Function: supabase functions deploy match-listeners, set env vars SPOTIFY_CLIENT_ID + SUPABASE_SERVICE_ROLE_KEY in the Dashboard, then schedule with pg_cron (comment at top of the function has the exact SQL)
  5. Run: npx expo start