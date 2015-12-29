---
title: How to list all files larger/smaller than certain size
author: fellipe
layout: post
permalink: /2014/09/how-to-list-all-files-largersmaller-than-certain-size/
perfect_quote_author:
  - 
perfect_quote_where:
  - 
sharepress_meta:
  - 'a:7:{s:7:"enabled";s:2:"on";s:7:"message";s:156:"<!--:en-->How to list all files larger/smaller than certain size<!--:--><!--:pt-->Como listar todos os arquivos maiores/menores que um certo tamanho<!--:-->";s:11:"description";s:105:"If you want to list all flac files smaller than 12mb: find -name "*.flac" -size -12000k If you want to...";s:4:"link";s:91:"http://code.fellipebrito.com/2014/09/how-to-list-all-files-largersmaller-than-certain-size/";s:4:"name";s:156:"<!--:en-->How to list all files larger/smaller than certain size<!--:--><!--:pt-->Como listar todos os arquivos maiores/menores que um certo tamanho<!--:-->";s:7:"targets";a:1:{i:0;s:4:"wall";}s:7:"picture";s:76:"http://code.fellipebrito.com/wp-content/plugins/sharepress/img/wordpress.png";}'
sharepress_twitter_meta:
  - 'a:1:{s:7:"enabled";s:3:"off";}'
sharepress_error:
  - A user access token is required to request this resource.
categories:
  - Uncategorized
---
If you want to list all flac files smaller than 12mb:

<pre class="lang:default decode:true">find -name "*.flac" -size -12000k</pre>

If you want to list files bigger than, just change the **- **for a **+**

<pre class="lang:default decode:true">find -name "*.flac" -size +12000k</pre>

Now if you want to delete them, just add a -delete after that:

<pre class="lang:default decode:true">find -name "*.flac" -size -12000k -delete</pre>