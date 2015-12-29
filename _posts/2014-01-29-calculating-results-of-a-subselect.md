---
title: Calculating results of a subselect
author: fellipe
layout: post
permalink: /2014/01/calculating-results-of-a-subselect/
perfect_quote_author:
  - 
perfect_quote_where:
  - 
categories:
  - sql
  - subselect
  - substring
  - substring_index
tags:
  - mysql
  - sql
  - subselect
  - substring
  - substring_index
---
Problem:  
I have a column with the a video&#8217;s duration in a string &#8220;duration &#8211; 4:34&#8243;; I need to know how many seconds this video has.

Solution:  
<a href="http://dev.mysql.com/doc/refman/5.0/en/string-functions.html" target="_blank">MySQL</a> has a method <a href="http://dev.mysql.com/doc/refman/5.0/en/string-functions.html#function_substring-index" target="_blank">SUBSTRING</a> (<a href="http://dev.mysql.com/doc/refman/5.0/en/string-functions.html#function_substring-index" target="_blank">MySQL Manual</a>) that helps me to split the string so I can easily calculate it (without use sum), and&#8230; voila!

<pre title="Calculating results from a subselect">SELECT minutes, seconds, 
       (minutes*60)+seconds as total_seconds 
       FROM (
	SELECT 
			TRIM(SUBSTRING_INDEX(SUBSTRING_INDEX(duration, ':', 1), '-', -1)) AS minutes,
			TRIM(SUBSTRING_INDEX(SUBSTRING_INDEX(duration, ' ', 3), ':', -1)) AS seconds
		FROM video
		 	WHERE duration IS NOT NULL
		 	LIMIT 0, 100
) as videos_subselect</pre>