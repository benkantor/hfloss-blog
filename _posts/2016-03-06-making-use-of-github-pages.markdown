---
layout: post
title:  "Making Use of Github Pages"
date:   2016-03-06 20:30:00
categories: blog
---

## Introduction

Having a website for your FOSS project can be helpful as it can serve as a
centralized location for documentation, learning, and onboarding resources. If
you use Github to host your project, you can use Github Pages to create a free
static websitefor your project. Github allows you to have one website per User
or Organization account, and an additional website per repository.

In this blog post I will do a walkthrough of setting up github pages websites.

## Creating your User or Organization Website

Github Pages websites for projects are served as a subdirectory of your User or
Organization website, so you'll want to create the User or Organization website
first.

Create a new repository for your user or organization with the following name
format:

`username.github.io` or `org_name.github.io`

After a few minutes, Github will start serving the files in the master branch
of this repository as a website that you can reach at `username.github.io`

Github has built in support for [Jekyll][Jekyll], a blog aware static site
generator. This means that if you decide to use Jekyll for your website, 
Github will automatically build and serve a Jekyll project in the master branch
of the repository. 
 
While Github has built in support for Jekyll, as long as your website is only
static content, you can use any other web frameworks. To do this, you can
simply push your already built code to the repository.

## Creating a Project website

1. Clone the repo of the project you want to make a website for.

```
git clone myproject.git
```

2. Make an orphan gh-pages branch in your repo

```
cd myproject
git checkout --orphan gh-pages
```

An orphan branch has no parent commits and has a completely separate history
from the rest of your project. This means that you can keep your website code
in the orphan branch and have it be completely isolated from your project code.

3. Remove the existing project code

```
rm -rf .
```

4. Add your website code

5. Commit and push the branch

```
git push -u origin gh-pages
```

Now your new project website will be accessible at
`username.github.io/project_name`

For more info on Github Pages, check out their [doc page][doc_page]


[jekyll_website]: https://jekyllrb.com/
[doc_page]: https://help.github.com/categories/github-pages-basics/

