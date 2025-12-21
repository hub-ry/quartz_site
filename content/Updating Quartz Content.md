
I feel i have not been doing this most efficiently but this is my log of how I have been doing it as of 12-13-25.

Context: Quartz builds straight html from markdown, so I found it necessary to host the website from a separate branch named `gh-pages`. This contains the build **output** from running the site, or specifically `npx quartz build`. 

The fastest way I have found to update the `gh-pages` branch is to rebuild in main, then go into the public folder (default build output) and just commit using the origin gh-pages. 

Note: if you only have gh-pages on github but not local run 
`git fetch origin` ~ this fetches everything you don't have
`git checkout gh-pages` ~ assuming gh-pages was a github branch to begin with 
and fetch was successful 


Maybe full guide below:

```
npx quartz build
cd public
git add -A
git commit -m "Add new content"
git push -f origin gh-pages
cd ..
```



#### UPDATED:

```
npx quartz build
git branch -D gh-pages
git subtree split --prefix public -b gh-pages
git push -f origin gh-pages
git checkout main
```