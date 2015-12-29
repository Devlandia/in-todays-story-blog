---
title: "Resizing splits"
meta_description: Sometimes I want to read a manual, a helper, a README, or even just want to read my code in 'full screen'. This is how I do it.
layout: post
permalink: resizing-splits
categories: [vim]
---
One of the things I most like in VIM is the easy way to split its environment. Using VIM splits + [ctrlP](https://github.com/kien/ctrlp.vim) + [tMux](http://en.wikipedia.org/wiki/Tmux) makes me a lot more productive.

Sometimes I want to read a manual, a helper, a README, or even just want to read my code in 'full screen'. This is how I do it:

Maximize the current sprint in the vertical:
{% highlight vim %}
ctrl + w _
{% endhighlight %}
> _ctrl + w means you have to press the key Ctrl and the key w at the same time and then release them to press the next key_

Maximize the current sprint in the horizontal:
{% highlight vim %}
ctrl + w |
{% endhighlight %}

Resize all splits to be the same (also called 'normalize')
{% highlight vim %}
ctrl + w =
{% endhighlight %}

Ask for help! VIM's helper is pretty useful, let's say you like the examples above and want to go further. I'd suggest that before you google it, you invest some time reading VIM's help.
{% highlight vim %}
:help :split
{% endhighlight %}
