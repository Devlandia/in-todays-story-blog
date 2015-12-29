---
title: Fatal error while bundling capybara-webkit
meta_description: Fatal error while bundling capybara-webkit (0.10.1) with native extensions
layout: post
permalink: fatal-error-while-bundling-capybara-webkit
categories: [capybara, cucumber, ruby, terminal, unix]
---
The error:

{% highlight bash %}
Fatal error while bundling capybara-webkit (0.10.1) with native extensions
{% endhighlight %}

How to fix:

{% highlight bash %}
apt-get install qt4
gem install capybara-webkit -v '1.1.0'
{% endhighlight %}

If you need further information read [here](https://github.com/thoughtbot/capybara-webkit/wiki/Installing-Qt-and-compiling-capybara-webkit){:target="_blank"}

You're welcome.
