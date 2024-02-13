+++
title = "Blog Created with Hugo"
date = 2022-05-14T07:07:07+01:00
draft = false
+++

Like everyone else and their dog, I set up this blog website to post about personal projects in technology and other fun topics. 

Set up this blog website with Hugo Project and PaperMod Theme on mac computer:

----------

## Doc URLs:

### Hugo Docs:
- https://gohugo.io/documentation/

### PaperMod Docs:
- https://github.com/adityatelange/hugo-PaperMod/wiki/Features

### Hugo Deployment types:
- https://gohugo.io/getting-started/usage/

-----------

## Deployment:

### Hugo Local Install and Server:
    - Mac Terminal:
        - `Brew Install Hugo`
        - `git init`
        - `git submodule add https://github.com/adityatelange/hugo-PaperMod/wiki/Features#profile-mode themes/hugo-PaperMod`
        - `hugo server -D`

### Publish Files to Public Folder
    - Go to project in terminal
        - Build the published version by running:
        `hugo`

### GitHub Pages Deployment:
    - Go to Github.com:
        - Login
        - Create a new repository named <username>.github.io, filling in your username
            - Create without readme
            - Make public
    - Go back to local terminal in project location:
        - Point to github origin location:
            - `git remote add origin https://github.com/<username>/test.git`
            - `git branch -M main`
            - `git push -u origin main`
    - Go back to Github.com
        - Wait for deployment to be done

    - Check out deployment
        - Go to Settings
        - Go to Pages
        - Select published site https://<username>.github.io/

** Note ** You will only have the ReadMe page come up for this. You need to specify it is a hugo project. 

### Create Build File with Github Actions:
    - Go to Settings tab
    - Go to Pages
    - Under Build and Deployment select GitHub Actions
    - Search for Hugo
    - Commit and push hugo build file to repository

If you don't have any posts that show up it is because the "draft" flag in the post is not set to false. You will need to set that to false and build the server again with `hugo`. Recommit and push the repository and you will see the new post. 

Hope there are good things to come!

![Alt text](/images/IMG_0507.jpg "a title")