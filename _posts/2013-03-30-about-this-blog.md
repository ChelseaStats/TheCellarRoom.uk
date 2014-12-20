---
layout: post
title: About this blog
description: How I setup this blog and what I use to run it
---
So, I've just finished up setting up this brand new blog. Before I've always run WordPress or Tumblr, but since WordPress is kind of over-kill with what seems like heavy memory usage that makes my host angry and Tumblr has it's ups and erm downs, I've decided to try something new, so this time I am running a static blog with [Jekyll](http://jekyllrb.com/).

>Jekyll is a simple, blog aware, static site generator. It takes a template directory (representing the raw form of a website), runs it through Textile or Markdown and Liquid converters, and spits out a complete, static website suitable for serving with Apache or your favorite web server. This is also the engine behind GitHub Pages, which you can use to host your project’s page or blog right here from GitHub.

So after I started using jekyll, I don't need any database server, because everything is stored in static files. It also means I can use whatever editor I want to use (TextMate or vim) to write my blog posts in markdown. I'm going to go with the gorgeously simple iA Writer. 

So if I want to publish a new post, I simply open up iA Writer and type, I save the file into my local repo and push it up to github, as they host the site. 

{% highlight sh %}
git add .
git commit -m "Added new content"
git push origin master
{% endhighlight %} 

And that will push my new post over to my server and it will be live on the internet.

I love this solution, it's so simple and it super lightweight, since all the web server will need do is just serving some static files, and not generating dynamic content in some scripting language and fetching content from a database server, like it would do if I used something like WordPress.

This will hopefully allow me to write more... even more so now that github has a web interface for creating new files.
