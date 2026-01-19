---
tags:
  - Forest
  - Version-Control-Notes
---


# 1. Make sure your work is committed on your feature branch
git checkout ryan
git status
git add .
git commit -m "Your message here"

# 2. Update main with the latest from GitHub
git checkout main
git pull origin main

# 3. Merge your branch into main (safe, local)
git merge ryan
# - If conflicts appear: fix them in your editor, then:
#   git add .
#   git commit

# 4. Push the updated main branch to GitHub
git push origin main

# 5. (Optional) Delete the branch after successful merge
git branch -d ryan
