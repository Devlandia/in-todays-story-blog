---
title: How to set your unix default editor
meta_description: I can't count how many times in the past I had troubles with unix complaining I don't have a default editor. To fix this issue is ridiculously simple
layout: post
permalink: how-to-set-your-unix-default-editor
categories: [alias, terminal, ubuntu, unix, vim]
---
I can't count how many times in the past I had troubles with unix complaining I don't have a default editor.

To fix this issue is ridiculously simple: just edit your [bashrc](http://en.wikipedia.org/wiki/Bash_(Unix_shell)){:target="_blank"} and add this line:

{% highlight bash %}
export EDITOR='vim'
{% endhighlight %}
