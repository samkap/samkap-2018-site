---
title: Quick performance boost on the site
date: 2017-11-14 19:16:00 -06:00
published: false
layout: post
---

I'm sitting at home, with a sore throat and an almost-gone fever. With Firefox's new blazing fast, Quantum, I can't help think about it and conversely, my lack of performance while sick. In order to cheer myself up and feel mildly productive, I thought I'd pick apart my site with a few accessibility tools and speed up the performance speed a tad. I'd writing this as I go through each step. The following are the steps I took LIVE:

## 1. First, re-read Dave's posts on RWD Bloats: [one]() and [two]().

Based on Dave's advice, check my grades with quick tests from [Google PageSpeed](https://developers.google.com/speed/pagespeed/insights/) and [WebPageTest](https://www.webpagetest.org/).

### Google PageSpeed

![desktop-01-start.png](/uploads/desktop-01-start.png)
Both Mobile and Desktop have the same issues. According to Google, two important things to fix are: "Eliminate render-blocking JavaScript and CSS in above-the-fold content" that can be broken up into a few steps, and "Leverage browser caching", which I have no idea how to do, yet.

![desktop-02-start.png](/uploads/desktop-02-start.png)
These are things I'm not being lazy about, at least on this page, but I'm glad that images are optimized (yay [ImageOptim](https://imageoptim.com/) but if you know of a great Jekyll plug-in that could do this, let me know!

![webpagetest-start.png](/uploads/webpagetest-start.png)
Yay! Only one F! This is *just *like school all over again. Kidding. But according to this Typekit is out of control, making up over 54-point-freaking-7-percent (54.7%) of my site's bytes. That seems like a lot and I don't like. Also, I have six images on home, and I don't quite see why until favicons have anything to do with it. Now armed with knowledge, let's see what we can do about it. Here goes!

## 1. Moved Typekit to below my content

So, before you get mad at me, know that I'm mad at me. I do know better, I was being lazy for a long time. So now my Typekit codes, live in a `scripts` includes file that is included after my `</body>` tag.

## 2. Mess with Typekit Settings

![typekit-01.png](/uploads/typekit-01.png)
Log into Typekit and see if I'm missing any optimization settings there. My kit is 64k, 54k if I don't keep opentype feature. For now, I will keep it on and maybe come back to this later.

![typekit-02.png](/uploads/typekit-02.png)
I jumped into my Kit Settings and saw a "Optimize performance" option. It links to [more info](https://helpx.adobe.com/typekit/using/optimizing-performance.html), which states:

> Increasing the cache timeout means that you will no longer be able to make quick changes to this kit. When this option is enabled, updates may take up to a week to be visible to all your visitors; disabling the option won’t take full effect until after a week, either. Use this option only if you don't plan to make any further changes to your kit.

This is interesting and I don't need to change my fonts any time soon, so I check it.

\## 3. Now, this six image thing

Okay, so it is favicons. I don't need six. I should only have three, I think. One favicon, that photo of me, and my logo. The other three are coming, mainly for the purpose of serving as icons on mobile devices. I don't know about anyone else, but I don't even have my own site on my home screen. I feel like this is unnecessary to keep, so I take it out of my `head` includes, and in the process, clean up spaces and unused code in six other includes. I feel better about it, but I'm not sure if it's actually helping yet.

I also, re-optimized my logo (7k, no change) and the photo at the bottom of me (

