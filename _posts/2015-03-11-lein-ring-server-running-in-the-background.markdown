---
title: "Lein Ring Server running in the background"
meta_description: there has been an awakening in the force.
layout: post
permalink: lein-ring-server-running-in-the-background
categories: [shell, clojure]
---
I've been working on a study case that has as a main target to run two different servers at the same time - one for the backend and the other for the frontend. [front-back-case](https://github.com/fellipebrito/front-back-case){:target="blank"}.

In order to not lose time and type less, I've been creating scenarios for every back/front server combination. So I can start and kill them with only one line. [Here are some of the scripts to start and kill servers](https://github.com/fellipebrito/front-back-case/tree/master/bin){:target="blank"}

Today, after I code a simple server in Clojure, I had to figure out how to start a ring server in the background. After few minutes looking for a solution I realised that I could do it using nohup:

{% highlight bash %}
nohup lein ring server-headless 8080 >/dev/null 2>&1 &
{% endhighlight %}
