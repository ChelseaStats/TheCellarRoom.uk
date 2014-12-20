---
layout: post
title: SQL lesson 101
description: some coding that caught us out
date: 2013-10-22 10:00:00

---


Today's SQL lesson:

    SELECT SUM( a ) , SUM( b ) , SUM( c ) 
    FROM (
      SELECT 2 AS a, 2 AS b, 2 AS c
      FROM dual
      UNION ALL 
      SELECT 3 AS a, 4 AS c, 5 AS b
      ) a
      

The order of the fields is important here  a,b,c + a,c,b does not equal a+a, b+b, c+c as you might expect.

