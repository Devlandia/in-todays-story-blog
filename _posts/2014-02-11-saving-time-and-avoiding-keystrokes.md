---
title: Saving time and avoiding keystrokes
meta_description: Our brains are incredibly fast, as well as our computers. We should not decrease this speed, with our slow fingers or too many keystrokes. It is important to avoid unnecessary typing. One way to do that is creating some aliases
layout: post
permalink: saving-time-and-avoiding-keystrokes
categories: [alias, terminal health]
---
Our brains are incredibly fast, as well as our computers. We should not decrease this speed, with our slow fingers or too many keystrokes. **It is important to avoid unnecessary typing. **

One way to do that is **creating some aliases** on the shell, which improves our speed but also avoids some good amount of keystrokes,  saving your health in the long term.

Please, do some simple math with me: if you type *'git status'* 20 times a day, it is 100 times per week, 400 times per month and ~5000 times per year.  
In a professional lifetime, you'd type these 10 keystrokes, > 100.000 times,  which gives us an incredible mark of **1 MILLION keystrokes just to know what has changed in our code**.

I use *'gst'* as an alias. It **saves me 7 keystrokes per time**, which is > 60% of the total keystrokes. We can say that I will avoid more than **500.000 keystrokes in my dev lifetime** (20 years?!?).  And it is only one of my aliases.

So you can ask me to share  my aliases with you, and I'd gladly do that, actually, take a look on my dotfiles here (<a href="https://github.com/fellipebrito/dotfiles" target="_blank">https://github.com/fellipebrito/dotfiles</a>) however keep in mind that they are my customized alias, of course you can use that, but it would be better to know which commands you use often, would not it?

In order to help you (and help me) I am always watching screencasts and trying to capture new stuff that good developers are doing out there (You also might go to github, read  a bunch of public repositories, it is a great way to learn a lot with those guys), so <a href="http://codeulate.com/" target="_blank">Ben Orenstein</a> came up with this idea in his <a href="http://goruco.com/" target="_blank">GoRuCo</a> conference (and he also confirms he did not create that but grabbed it from the internet). (*if you are humble and smart enough you will see that you can learn a lot with the content that is already out there and  you can accept that at least 70% of what you code was inspired or copied from something else.*)

Well, less talk more code. If you want to know which aliases you should create, to know which are your top 20 most recurrent commands on the terminal, just use this command:

{% highlight bash %}
history | awk '{a[$2]++}END{for(i in a){print a[i] " " i}}' | sort -rn | head -20
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
5 ping
{% endhighlight %}
