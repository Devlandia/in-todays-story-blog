---
title: Calculating results of a subselect
meta_description: Problem is I have a column with the a video's duration in a string duration and I need to know how many seconds this video has.
layout: post
permalink: calculating-results-of-a-subselect
categories: [mysql, sql, subselect, substring, substring_index]
---
Problem:
I have a column with the a video's duration in a string "duration - 4:34"; and I need to know how many seconds this video has.

Solution:
<a href="http://dev.mysql.com/doc/refman/5.0/en/string-functions.html" target="_blank">MySQL</a> has a method <a href="http://dev.mysql.com/doc/refman/5.0/en/string-functions.html#function_substring-index" target="_blank">SUBSTRING</a> (<a href="http://dev.mysql.com/doc/refman/5.0/en/string-functions.html#function_substring-index" target="_blank">MySQL Manual</a>) that helps me to split the string so I can easily calculate it (without use sum), and&#8230; voila!

{% highlight mysql %}
SELECT minutes, seconds, 
       (minutes*60)+seconds as total_seconds 
       FROM (
  SELECT 
      TRIM(SUBSTRING_INDEX(SUBSTRING_INDEX(duration, ':', 1), '-', -1)) AS minutes,
      TRIM(SUBSTRING_INDEX(SUBSTRING_INDEX(duration, ' ', 3), ':', -1)) AS seconds
    FROM video
      WHERE duration IS NOT NULL
      LIMIT 0, 100
) as videos_subselect
{% endhighlight %}
