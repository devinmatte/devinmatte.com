---
layout: post
title:  Compressing with Webp
subtitle: Using Webp to improve performance
description: Webp can be used to compress files losslessly for better site performance
date:   2017-09-27 22:05:00
categories: webp
featured-image: https://devinmatte.github.io/images/posts/2017-09-27-before.png
thumbnail-image: https://devinmatte.github.io/images/posts/2017-09-27-before.png
comments: true
author: Devin Matte
author-image: https://avatars3.githubusercontent.com/u/9310513
author-bio: Second Year Software Engineering Student at Rochester Institute of Technology
---

One of the biggest bottlenecks for everyday sites, are images. 
When you run a [chrome audit](https://developers.google.com/web/updates/2017/05/devtools-release-notes) now, one of the biggest hits on performance, is your images. 
Images are treated like render blocking assets by a lot of browsers. 
Which means, your page is going to appear as though it's taking longer to load while it waits on images.
You know what it's like when you visit a page and the page loads, before the image in the background, and you watch the white transition away to reveal the image.
That's not really ideal. 
The faster your page loads, the better for your users, which in turn is better for your page views.

![Before Webp](https://devinmatte.github.io/images/posts/2017-09-27-before.png)

When you run the chrome audit, one of the recommendations to improve performance is to use `webp`. I was ignoring that advice for a while for a lack of understanding, due to google's poor documentation of how to set it up.
However one day I just decided to give it a go, and here is how you can go ahead and do it yourself for those sweet performance improvements.