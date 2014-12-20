---
layout: post
link: http://snipplr.com/view/70489/find-all-links-on-a-page/
title: Find All Links on a Page
description: Using the DOM, you can easily grab all links from any webpage
date: 2013-10-31 21:00:00

---

Using the DOM, you can easily grab all links from any webpage. Here’s a working example:

    $html = file_get_contents('http://www.example.com');
    $dom = new DOMDocument();
    @$dom->loadHTML($html);
    // grab all the on the page
    $xpath = new DOMXPath($dom);
    $hrefs = $xpath->evaluate("/html/body//a");
    for ($i = 0; $i < $hrefs->length; $i++) {
           $href = $hrefs->item($i);
           $url = $href->getAttribute('href');
           echo $url.'<br />';
    }

