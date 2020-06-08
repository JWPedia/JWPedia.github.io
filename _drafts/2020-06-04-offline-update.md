---
layout: post
title: An Update On: Offline by Default 
permalink: /offline-update/
categories: technology minimalism
date: 2020-06-04
---

I [previously](offline) wrote about the idea of going offline by default. This experiment, which I had somehow forgotten about, has naturally resurfaced as a part of my life during the summer break. 

This summer, I am back at my home country Korea and occupied with a few but important tasks: 

1. Taking online summer courses for college. (Introduction to Probability, Data Structures and Algorithms.) 
2. Tutoring a few IB students on Math and Physics. 
3. Self-studying for GRE, Theory of Computation (next semester's class), and other intriguing subjects such as Computer Networking. 

All of these tasks require non-significant amounts of focused effort, whether that be watching lectures, solving exercise questions, or preparing to teach.  

In my pursuits to excel in my studies, as someone fortunate enough to be able to do it full-time, I've been tackling the same online vices. It's gotten to the point where I installed Activity watch, a FOSS passive time tracker for desktop computers, to find out that I spent a whopping 24 hours on social media and video games in a single weekend. Twenty-four freaking hours! Now that's some time I want back. 

While the specific vices may differ by person, my biggest time sinks are, in order of time spent: Youtube, Reddit, Discord, Overwatch, and Hearthstone. While there are other sources of distraction, their effects were negligible. For instance, single-player games rarely drew me in for more than an hour at a time, while the aforementioned online games kept me playing for hours. 

As such, I've re-started my quest to live offline by default. Not only are there repurcussions if I start slacking off on my summer courses or my tutoring gig, I've come to appreciate just how fortunate my situation is, and that I must learn as much as I can in two years or so of my life dedicated solely to learning. 

Practically, I've taken the following measures to limit my online time: 

* I completely blocked Youtube, Reddit, Discord, and few other potentially distracting websites by editing the `/etc/hosts` file. For reference, add the following lines for every website you wish to block:

```
127.0.0.1 website.com
::1 website.com
127.0.0.1 www.website.com
::1 www.website.com
```

* I turn off networking completely on my PC by default. I've scheduled 7PM to 8PM as the daily internet block. In this one-hour window, I will check and correspond to emails; download lecture materials, books, and anime episodes; archives webpages for later reading; submit assignments; and Google any questions I couldn't resolve in the previous day. 
* I still allow myself to temporarily enable internet for Zoom videoconferencing, for both my online classes and tutoring gig. After the class ends, I'm back offline. Another exception is using online coding practice websites such as LeetCode or Project Euler purely for the purposes of checking my answers. 
* I uninstalled all distracting apps on my iPhone except mission-critical communication apps such as Wechat and Kakaotalk, which people often use to contact me for important purposes. For this reason, my iPhone is allowed to have wifi turned on at all times. (I've never struggled with excessive texting on my phone, so this is not a big issue for me.) However, using Screen Time's Content Restriction capabilities, I disabled web browsing and installing of new apps. I also downloaded maps.me, a FOSS Google Maps alternative that supports downloading map data offline. My phone is, practically, a camera that does some texting and some navigation. 
* My iPad is used solely as a content consumption device. To avoid mindless web browsing, I disabled Safari with the same method as my iPhone. The only content available on my iPad is those synchronized from my PC with pCloud, or books from the official O'Reilly app. 

Although I'm merely a few days into this challenge, I am already experiencing several positive effects. 

* First and foremost, I can actually fall asleep now. I get tired at night, and sleep comes naturally - something I've struggled to do for ages. 
* I am more inclined to feel motivated to do physical exercise. Since there arent' any readily accessible forms of entertainment, barring pre-downloaded anime episodes and reading books, hiking at the backdoor mountain is a much more appealing activity.
* My productivity has risen, of course. 
* Even more important than the raw output of my work is its quality. Since I've consolidated Googling to one hour per day, I've been forced to use my own cognitive functions and the power of reading over the textbook one more time. As I've said [before](think), many a problems can be more deeply understood by thinking about it one more time before Googling it. 
