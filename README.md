# technical-writing
technical-writing docs

## Quick Start


https://vuepress.vuejs.org/guide/getting-started.html#prerequisites



npx create-vuepress-site [optionalDirectoryName]
npx create-vuepress-site technical-writing




## github deploying

source : https://vuepress.vuejs.org/guide/deploy.html#github-pages

Set the correct base in docs/.vuepress/config.js.

If you are deploying to https://<USERNAME>.github.io/, you can omit base as it defaults to "/".

If you are deploying to https://<USERNAME>.github.io/<REPO>/, for example your repository is at https://github.com/<USERNAME>/<REPO>, then set base to "/<REPO>/".

Inside your project, create deploy.sh with the following content (with highlighted lines uncommented appropriately), and run it to deploy:


```sh
#!/usr/bin/env sh

# abort on errors
set -e

# build
npm run docs:build

# navigate into the build output directory
cd docs/.vuepress/dist

# if you are deploying to a custom domain
# echo 'www.example.com' > CNAME

git init
git add -A
git commit -m 'deploy'

# if you are deploying to https://<USERNAME>.github.io
# git push -f git@github.com:<USERNAME>/<USERNAME>.github.io.git master

# if you are deploying to https://<USERNAME>.github.io/<REPO>
# git push -f git@github.com:<USERNAME>/<REPO>.git master:gh-pages

cd -
```


> TIP
> You can also run the above script in your CI setup to enable automatic deployment on each push.

