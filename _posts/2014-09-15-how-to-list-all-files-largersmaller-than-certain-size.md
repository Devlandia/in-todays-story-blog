---
title: How to list all files larger/smaller than certain size
meta_description: If you want to list all flac files smaller than 12mb or bigger than or even delete them all.
layout: post
permalink: how-to-list-all-files-largersmaller-than-certain-size
categories: [bash, ubuntu]
---
If you want to list all flac files smaller than 12mb:

{% highlight bash %}
find -name "*.flac" -size -12000k
{% endhighlight %}

If you want to list files bigger than, just change the **- **for a **+**

{% highlight bash %}
find -name "*.flac" -size +12000k
{% endhighlight %}

Now if you want to delete them, just add a -delete after that:

{% highlight bash %}
find -name "*.flac" -size -12000k -delete
{% endhighlight %}
