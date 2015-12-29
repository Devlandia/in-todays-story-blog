---
title: How to update my remote branch information
meta_description: To clean-up your remote references, or only your local mess.
layout: post
permalink: how-to-update-my-remote-branch-information
categories: [git, github]
---
To clean-up your remote references:

{% highlight bash %}
git remote prune origin
{% endhighlight %}

If you want to clean up your local mess, you also can use:

{% highlight bash %}
git branch -r
{% endhighlight %}
