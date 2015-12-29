---
title: How to update my remote branch information
author: fellipe
layout: post
permalink: /2014/05/how-to-update-my-remote-branch-information/
perfect_quote_author:
  - 
perfect_quote_where:
  - 
sharepress_meta:
  - 'a:1:{s:7:"enabled";s:3:"off";}'
sharepress_twitter_meta:
  - 'a:1:{s:7:"enabled";s:3:"off";}'
categories:
  - Uncategorized
---
To clean-up your remote references:

<pre class="lang:default decode:true">git remote prune origin</pre>

If you want to clean up your local mess, you also can use:

<pre class="lang:default decode:true">git branch -r</pre>