---
title: How to set your unix default editor
author: fellipe
layout: post
permalink: /2014/02/how-to-set-your-unix-default-editor/
perfect_quote_author:
  - 
perfect_quote_where:
  - 
sharepress_meta:
  - 'a:1:{s:7:"enabled";s:3:"off";}'
sharepress_twitter_meta:
  - 'a:1:{s:7:"enabled";s:3:"off";}'
categories:
  - alias
  - terminal
  - ubuntu
  - unix
---
I can&#8217;t count how many times in the past I had troubles with unix complaining I don&#8217;t have a default editor.

To fix this issue is ridiculously simple:, just edit your <a href="http://en.wikipedia.org/wiki/Bash_(Unix_shell)" target="_blank">bashrc</a> and add this line<span style="line-height: 1.5;">:</span>

<pre class="lang:default decode:true" title="bashrc">export EDITOR='vim'</pre>