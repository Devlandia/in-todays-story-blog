---
title: Be more productive with TMUXINATOR
meta_description: TMUX is a software that lets you switch easily between several programs in one terminal, detach them and reattach them to a different terminal. Lets see how make it even more incredible
layout: post
permalink: be-more-productive-with-tmuxinator
categories: [alias, ruby, terminal, tmux, tmuxinator, ubuntu, unix]
---
<img alt="" src="https://f.cloud.github.com/assets/141213/916084/065fef7c-fe82-11e2-9c23-a9622c7d83c3.png" width="2560" height="1440" />

<a href="https://github.com/tmuxinator/tmuxinator" target="_blank">TMUXINATOR</a> is a <a href="http://en.wikipedia.org/wiki/Tmux" target="_blank">TMUX</a> session manager; <a href="http://en.wikipedia.org/wiki/Tmux" target="_blank">TMUX</a> is a software that lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal. And do a lot more. See <a href="http://www.openbsd.org/cgi-bin/man.cgi?query=tmux&sektion=1" target="_blank">the manual</a>.

Requirements:
- <a href="/how-to-set-your-unix-default-editor/" target="_blank">Define your bash $EDITOR</a>;
- <a href="http://rvm.io/rvm/install" target="_blank">Ruby installed</a>
- TMUX 1.8+ installed, if you have any troubled installing this version in your Ubuntu <a href="http://askubuntu.com/a/324949" target="_blank">you can follow these tips</a>.

<a href="https://github.com/tmuxinator/tmuxinator" target="_blank">TMUXINATOR</a> is a rubygem, to install it is easy:

{% highlight bash %}
gem install tmuxinator
{% endhighlight %}

After you install it you can start a new project using:

{% highlight bash %}
tmuxinator open my_project
{% endhighlight %}

This command will open a YAML file inside your default editor (that I wish to be VIM):

{% highlight yaml %}
# ~/.tmuxinator/my_project.yml

name: my_project
root: ~/

# Runs before everything. Use it to start daemons etc.
# pre: sudo /etc/rc.d/mysqld start

windows:
  - editor:
      layout: main-vertical
      panes:
        - vim
        - rspec
  - server: bundle exec rails s
  - logs: tail -f logs/development.log
{% endhighlight %}

If you only read this file you will be amazed with all the possibilities it gives to you. This basic config file is really useful if you work with a Rails project. It gives to you three windows ( rspec and editor, server and log reader ) ready to dive in code.<span style="line-height: 1.5;"><br /> </span>

Well, with this file saved you can start your day typing:

{% highlight bash %}
mux start my_project
{% endhighlight %}

That&#8217;s it, your whole dev environment is active and ready to rumble. You can configure it as you wish: you need a ssh connection, new editors, a database window, top, capistrano? You can do it and much more, explore its manual and you will see how powerful it is.

You can also share its .conf with your team and avoid those 15 minutes every developer loses to start to code in the morning.

Now let&#8217;s do a simple math. Saving 15 minutes everyday * 20 days you **save 5 hours of work per month per developer**.

Now multiply this &#8220;save time&#8221; * your dev team (8 devs?!?). You are saving A WEEK of time and money with this simple config file.

Cheers to productivity and money being saved!
