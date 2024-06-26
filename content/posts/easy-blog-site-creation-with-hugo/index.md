+++
title = 'Easy Blog Site Creation with Hugo'
date = 2022-05-14T07:07:07+01:00
tags = ['Programming','Web Development', 'Hugo']
draft = false
+++

Like everyone else and their dog, I set up this blog website to post about personal projects in technology and other fun topics. 

## Components Used:
- Mac
- Hugo
- PaperMod
- GitHub Pages

-----------

## Local Deployment:
In Local Machine:
 1. `Brew Install Hugo`
 2. `git init`
 3. `git submodule add https://github.com/adityatelange/hugo-PaperMod/wiki/Features#profile-mode themes/hugo-PaperMod`
 4. `hugo server -D`
 5. Go to: <http://localhost:1313>
 6. Stop Server: Ctrl C

## GitHub Pages Deployment:
In Github.com:
  1. Create new repository named `<username>.github.io`, filling in your username
   
In Local Machine:
   1. `git remote add origin https://github.com/<username>/<username>.github.io.git`
   2. `git branch -M main`
   3. `git push -u origin main`

**Nothing will show up. Will need to tell GitHub it is a Hugo project**

## Create Build File with Github Actions:
In GitHub.com:
   1. Go to Settings tab
   2. Go to Pages
   3. Under Build and Deployment select "GitHub Actions"
   4. Search for "Hugo"
   5. "Commit and Push" hugo build file to repository

## Create and Display Post
In Local Machine:
   1. `hugo new content posts/<postname>.md` Filling in a postname you want
   2. Place content in post
   3. In Front Matter (markdown header) set "draft" to "false"
   4. `hugo`
   5. `git add .`
   6. `git commit -m <message>`
   7. `git push`

**You should now see a working Hugo Site at `https://<username>.github.io`.**

### Add Custom Domain (Optional):
In Github.com:
   1. Go to Settings tab
   2. Go to Pages
   3. Under Custom Domain add your custom domain
   4. Will take a while to do DNS check
   5. Make sure your DNS records are pointing to github correctly


----------

## Doc URLs:

- [Hugo Docs](https://gohugo.io/documentation/)
- [PaperMod Docs](https://github.com/adityatelange/hugo-PaperMod/wiki/Features)
- [Hugo Deployment types](https://gohugo.io/getting-started/usage/)

Hope there are good things to come!

![Alt text](/posts/easy-blog-site-creation-with-hugo/good-bad.jpg "a title")