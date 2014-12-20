---
layout: post
title: Joomla 3.1.1 quirks
link: http://docs.joomla.org/Help31:Content_Article_Manager_Edit
date: 2013-06-24 18:00:00
---

It turns out that you can override the default.php layout/template for your joomla 3.1.1 article by copying the file and editing it in your 
<pre>
templates/ templatename/ html/ com_content/ article/ default.php
</pre>

But if you want to create some alternative layout options that content authors can select from the drop down box in the admin panel, you can't have the default.php in your template.

You have rename this file and select it manually for each article (even if this means all but one of them).

What a pain in the arse.
