###### thecellarroom.net/blog/

> TheCellarRoom.net Blog




###### Guide

To start a jekyll server in terminal `cd` to the directory and type

    jekyll serve --watch
    
to stop a jekyll server

   `CTRL` `C`

   
site structure is usually like this

    .
    |-- _config.yml
    |-- _includes
    |-- _layouts
    |   |-- default.html
    |   `-- post.html
    |-- _posts
    |   |-- 2007-10-29-blog-posts-that-are-just-a-list-suck.md
    |   `-- 2009-04-26-blog-posts-that-start-with-a-why-suck.md
    |-- _site
    `-- index.html

In addition it is a good idea to define a `.gitignore` that contains that `_site` directory. 

Usually it is something you do not want to version.

* Category Page - Jekyll

simply copy this as a file into your Jekyll set up in a folder which is the category name `/category/file.md`


 ```ruby
---
layout: layout
title: Category Title
author: authorname
---
<p>A list of articles written by {{page.author}}</p>
<ul class="posts">
{% for post in site.categories.*categorytitle* limit: 20 %}
  <div class="post_info">
    <li>
         <small><span>★ <a href="{{ post.url }}">{{ post.title }} →</a> :
         published  on {{ post.date | date:"%Y-%m-%d" }} </span></small>
    </li>
    </div>
  {% endfor %}
</ul>
 ```

* Related Posts

this is the quick method, it lacks some accuracy at times, but is speedier so worth it.


```ruby
<div id="related">
<h2>Related posts</h2>
<ul class="posts">
{% for post in site.related_posts limit:3 %}
<li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
</div>
```
