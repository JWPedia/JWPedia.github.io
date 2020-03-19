---
layout: post
title: A Minimal, Private Mac
permalink: /minimal-mac/
categories: technology digital-minimalism minimalism
date: 2019-09-26
---
![MacBook Desktop](/Media/minimal-mac.png)

This is what my Macbook's desktop looks like. It is free from all possible sources of distractions.

It would be difficult to focus if your workspace was littered with loose documents, empty coca-cola cans, stationeries, and doodles. The same principle applies to our digital environment.

As a tech-junkie and a computer science student, my laptop is the space that I spend most of my time in. So, I made it into the most focused setup possible.

It means that I will follow these rules:

1.  Reduce all visual clutter.
2.  Eliminate all potential interruptions.
3.  If a task that a digital tool performs is not highly valuable, eliminate said tool.
4.  Use the simplest technology that accomplishes a valuable task.
5.  Since advertisements are the enemy of minimalism, use the more private option when two options are otherwise comparable.

## Operating System

macOS is the simplest commercial desktop operating system. It has a minimalistic design language, and most things _just work_. Not only that, as a Unix-like OS, working in the command line - the most focused environment possible - is a breeze.

That being said, I do not want to police around which OS anyone uses. The rules above can be applied to every OS.

## OS-Level Settings

Here are all the OS-level settings I modify in System Preferences:

*   General
    *   Appearance: Dark
    *   Close windows when quitting an app
    *   Automatically hide and save the menu bar
*   Desktop & Screen Saver
    *   I chose an understated default wallpaper.
*   Dock
    *   Size: minimum
    *   Magnification: off
    *   Automatically hide and show the Dock
*   Mission Control
    *   Automatically rearrange Spaces based on most recent use: off
    *   Have only 1 Space open by default
*   Screen Time: on
*   Security & Privacy
    *   FileVault disk encryption: on
    *   Firewall: on
    *   Privacy: limit ad tracking, do not share analytics

## Notifications

Notifications inherently violate rule 3: eliminate all potential interruptions. There is only one place where notifications are allowed: out of my life.

In System Preferences > Notifications, I made some merciless changes.

*   Nothing goes to the Notification Center
*   No app may have a badge icon
*   Only Music and [Tomighty](tomighty.org) may send out a banner-style notification
*   Just in case I missed something, my MacBook is automatically put to Do Not Disturb mode from 9 to 6.

## File Management

My file management system has one goal - to be able to retrieve any needed file quickly from anywhere.

To do so, clearing the Downloads and Desktop folder every evening has to become habitual.

All of my files are stored in a single Documents folder that is synchronized to my devices via iCloud.

iCloud is the most secure cloud storage service out of the big-name options. Other alternatives, such as Google, Microsoft, and Amazon, can and will read your data. For stronger security, you may want to use a zero-knowledge cloud service such as [Sync.com](https://www.sync.com/).

Personally, iCloud is the sweet spot between convenience and security. With two-factor authentication enabled and a unique, frequently changed password, iCloud should be secure enough for most users.

Documents folder is set as the default folder when Finder opens.

![Document folder organization](/Media/minimal-finder.png)

This is what my Documents folder looks like. I use the tree view to quickly navigate through a deep folder structure with arrow keys.

The Images folder is where all of my photos live. While Photos is convenient to use, I have had my iPhoto library corrupted enough times to know that a simple folder tree with image files won't break in the next macOS update.

The Mastermind folder holds some files for organizing my time. I will defer explaining my rich text productivity system to a later post.

The Notable folder holds markdown notes. Markdown syntax is easy to learn, platform-independent, and unlikely to break so as long as plain text files exist. I edit markdown files in [Atom](https://atom.io/) with [markdown-preview-enhanced](https://atom.io/packages/markdown-preview-enhanced) package.

## My Favorite Apps

I will discuss some of these Apps and how I set them up in future posts. For now, remember that reducing visual clutter is rule 1 and that using the simplest technology that gets the job done is rule 5\. I stick to Apple apps as much as possible.

For further resource, check out Manu Moreale's posts on [minimal technology](https://manuelmoreale.com/minimal-technology), [simple browser](https://manuelmoreale.com/a-simple-browser), and [minimal email](https://manuelmoreale.com/emails).

![Firefox](/Media/firefox.png)

**Firefox** is the most private commercial browser.

![Mail](/Media/mail.png)

**Mail** is my email client of choice.

![Atom](/Media/atom.png)

**Atom** is my favorite text editor. It is what I use to take notes and code simple projects. Coding programs purely in a text editor and command line also happens to be an exercise to improve programming skills. I also use **IntelliJ IDEA**, **Xcode**, **ImageOptim**, and **Github CLI**.

![Tomighty](/Media/tomighty.png)

**Tomighty** is a free and simple pomodoro timer app with no bullshit.

**Calendar** is the simplest, functional calendar app.

**IINA** is my video player of choice. It is like VLC with a mac-native feel.

**Apple Music for Students** is my favorite music streaming service.

**iBooks** is my favorite way to read books.

While I try to stay away from it, **Microsoft Office** is also installed due to necessity.

## Conclusion

A minimal Mac setup takes little initial effort and can lead to higher productivity and clarity. I highly recommend any modern knowledge worker to follow some of the steps I described above.

In upcoming posts, I will discuss minimal iPhone and iPad setup, private web browsing, and rich text productivity system.
