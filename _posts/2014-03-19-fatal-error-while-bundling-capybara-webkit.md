---
title: Fatal error while bundling capybara-webkit
author: fellipe
layout: post
permalink: /2014/03/fatal-error-while-bundling-capybara-webkit/
perfect_quote_author:
  - 
perfect_quote_where:
  - 
sharepress_meta:
  - 'a:1:{s:7:"enabled";s:3:"off";}'
sharepress_twitter_meta:
  - 'a:1:{s:7:"enabled";s:3:"off";}'
categories:
  - capybara
  - cucumber
  - ruby
  - terminal
  - unix
---
The error:

<pre class="lang:default decode:true">Fatal error while bundling capybara-webkit (0.10.1) with native extensions</pre>

How to fix:

<pre class="lang:default decode:true">apt-get install qt4
gem install capybara-webkit -v '1.1.0'</pre>

If you need further information read <a href="https://github.com/thoughtbot/capybara-webkit/wiki/Installing-Qt-and-compiling-capybara-webkit" target="_blank">here</a>

You&#8217;re welcome.