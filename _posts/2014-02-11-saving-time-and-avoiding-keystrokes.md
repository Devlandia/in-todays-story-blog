---
title: Saving time and avoiding keystrokes
author: fellipe
layout: post
permalink: /2014/02/saving-time-and-avoiding-keystrokes/
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
tags:
  - alias
  - health
  - saude
  - terminal
---
[<img class="size-full wp-image-60 aligncenter" alt="77_83_ddd" src="http://code.fellipebrito.com/wp-content/uploads/2014/02/77_83_ddd.gif" width="278" height="283" />][1]

Our brains are incredibly fast, as well as our computers. We should not decrease this speed, with our slow fingers or too many keystrokes. **It is important to avoid unnecessary typing. **

One way to do that is **creating some aliases** on shell, which improves our speed but also avoids some good amount of keystrokes,  saving your health in the long term.

Please, do some simple math with me: if you type *&#8216;git status&#8217;* 20 times a day, it is 100 times per week, 400 times per month and ~5000 times per year.  
In a professional life time, you&#8217;d type  these 10 keystrokes, > 100.000 times,  which gives us an incredible mark of **1 MILLION key strokes just to know what has changed in our code**.

I use *&#8216;gst&#8217;* as an alias. It **saves me 7 key strokes per time**, which is > 60% of the total keystrokes. We can say that I will save more than **500.000 key strokes in my dev lifetime** (20 years?!?).  And it is only one of my aliases.

So you can ask me to share  my aliases with you, and I&#8217;d gladly do that, actually, take a look on my dotfiles here (<a href="https://github.com/fellipebrito/dotfiles" target="_blank">https://github.com/fellipebrito/dotfiles</a>) however keep in mind that they are my customized alias, of course you can use that, but it would be better to know which commands you use often, wouldn&#8217;t it?

In order to help you (and help me) I am always watching screencasts and trying to capture new stuff that good developers are doing out there (You also might go to github, read  a bunch of public repositories, it is a great way to learn a lot with those guys), so <a href="http://codeulate.com/" target="_blank">Ben Orenstein</a> came up with this idea in his <a href="http://goruco.com/" target="_blank">GoRuCo</a> conference (and he also confirms he did not create that, but grabbed it from internet). (*if you are humble and smart enough you will see that you can learn a lot with the content that is already out there and  you can accept that at least 70% of what you code was inspired or copied from something else.*)

Well, less talk more code. If you want to know which aliases you should create, in order to know which are your top 20 most recurrent commands on the terminal, just use this command:

<pre class="lang:sh decode:true" title="Example of 20 top commands">$ history | awk '{a[$2]++}END{for(i in a){print a[i] " " i}}' | sort -rn | head -20
100 ls
55 cd
49 git
43 vim
28 vagrant
19 vup
17 cat
13 source
13 fg
13 exit
12 pwd
12 open
10 rm
8 l
7 which
7 brew
6 sudo
6 mkdir
5 reset
5 ping</pre>

 [1]: http://code.fellipebrito.com/wp-content/uploads/2014/02/77_83_ddd.gif