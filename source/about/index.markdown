---
layout: page
title: "about"
date: 2015-03-11 11:09
comments: true
sharing: true
footer: true
---

# In today's story...

To write new posts you need to clone this repo and use the octopress based app.
You can find the documentation [here](http://octopress.org/docs/blogging).

The only think different is that you need commit on two places.

* You need access the folder source/_posts and make your commits there.
* After commit on source/_posts, come back to root path of project and commit.

This is because we using a different repo for posts.

After write the posts and run localy for tests (rake preview), you can invoce the task for deploy, as on [documentation](http://octopress.org/docs/deploying/github)