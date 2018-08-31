---
layout: post
title: 3 reasons PHP is outdated
date: 2018-08-31 09:35 -0600
author: Jacob Dick
description: PHP is a popular and widely-supported server language. Is it time to pull the plug on it?
---
My first journey into web development beyond HTML was with a SaaS company running a PHP app. I may be biased, since the app was written with CodeIgniter, but I wasn't impressed with the speed or scalability of this app as we grew our user base.

PHP has some inherent problems that aren't going away.

## PHP is synchronous

Many languages are inherently synchronous in nature. JavaScript, without Node.JS, is synchronous. Python enables asynchronous code through `asyncio`. But PHP is different. PHP [supports](http://php.net/pthreads) [threading](http://docs.php.net/Thread), but it isn’t quite the same as asynchronous code because of PHP’s next issue:

## Each request creates a separate PHP interpreter instance

WHAT?! I mean, it kind of makes sense when you think about the origins of PHP in 1995. But what about now? It costs resources to create an interpreter instance. The alternative is opening/starting the process and allowing it to run constantly. This is the route that Node and Django have taken.

## PHP is server-only

Although this isn’t that big of a deal, from a business perspective I’d rather have the same language on the front and back of my app.
