---
layout: post
title: Learning to Live in the Command Line, Part 1: Regolith + Pop!OS, Web Browsing
permalink: /cli-regolith/
date: 2020-04-09
categories: minimalism technology
---

I've long held a bit of a fascination on the command-line interface (CLI) while being scared to approach it. Experienced programmers have long since vouched for the power of the command line, its efficiency, and flexibility. Furthermore, as [Matt Might](http://matt.might.net/articles/cripple-your-technology/) recommends, the command line is extremely conducive to productivity, as there are little avenues for distractions. 

# Choosing a Linux Distro

Of course, if you're going to live and thrive in the command line, you should probably use Linux, the topic of this post. I had distro hopped around a bit in recent months, trying out everything from Ubuntu to Fedora to Manjaro. While I loved using the i3 tiling window manager with Manjaro, I missed some niceties that come with Ubuntu-based distros. 

1. There are extensive guides and articles online for troubleshooting Ubuntu. 
2. Non-English language support is more seamlessly baked in. 
3. I could never get my speakers to work in Manjaro, whereas Ubuntu-based distros come with nonfree drivers that ease the process. 
4. i3, while incredibly extensible, is a nightmare to set up. For instance, something as simple as changing the desktop wallpaper is a chore for beginners. 

That is when I stumbled into two projects that attempt to create a tiling window manager experience within GNOME: [Regolith](https://regolith-linux.org/) and [Pop! Shell](https://github.com/pop-os/shell). The former is a custom desktop environment built on top of i3 and GNOME. The latter, on the other hand, gives tiling window management capabilities into the Pop!OS desktop environment. Since the latter is not yet released, I settled with Pop!OS + Regolith as my Linux setup. 

Some may wonder why I didn't go with Ubuntu + Regolith, which works perfectly fine. Here's a few reasons why I chose Pop!OS over vanilla Ubuntu:

1. Pop!OS comes with less bloatware than Ubuntu. 
2. Pop!OS desktop environment looks more modern out of the box than Ubuntu. 
3. Pop!OS comes with the most recent drivers that ease the process of gaming on Linux. 
4. System76 behind Pop!OS have less controversies surrounding them than Canonical. 
5. System76's roadmap of their OS is incredibly promising, and I want in on the action. 

# Installing and Configuring Pop!OS

The installation process of Pop!OS was painless. I simply followed the [official docs](https://pop.system76.com/docs/install-pop-os/) and the on-screen prompt to erase the disk and install Pop!OS. 

Then, these were the first things that I did to set up my work environment: 

1. I troubleshot network connections. For some reason, the school's wifi only works if I set my IP address as "stable." 
2. I set up basic system settings with the bundled Settings app. I configured some keyboard shortcuts and input languages. In particular, I remapped screenshots as my keyboard doesn't have a PrintScreen key, and I remapped the shortcut for changing input language, as it was overriden by Regolith's default keybinding. 
3. I went ahead and uninstalled all unnecessary applications. 

These unnecessary applications are GUI apps that I plan to replace with CLI during this adventure. So Thunderbird, Gnome Calendar, Gnome Tasks, and any GUI text editors were exiled from my system. 

On the other hand, there are some GUI apps that I installed out of necessity: Zoom, Anki, pCloud Sync, and Discord. While some rudimentary command-line applications for these services exist, they do not meet my needs. For instance, offline sync capability for pCloud is only available via Electron GUI app. 

While I'd love to be able to completely substitute GUI web browsers with TUI web browsers for this experiment, some mission-critical websites rely on Javascript. Where possible, however, I will be using tools like [mps-youtube](https://github.com/mps-youtube/mps-youtube), [Newsboat](https://github.com/newsboat/newsboat), and [Links2](http://www.aboutlinux.info/2007/02/links2-cross-platform-console-based-web.html) where possible for internet media consumption. 

# Getting Used to Regolith (i.e. i3)

For those of us used to i3, Regolith is a similar and more polished out-of-the-box experience. It's a tiling window manager, which makes it suited for terminal windows. Regolith by default has different keybindings than Manjaro-i3 though. Luckily, a cheat-sheet can be opened at any time by pressing `SUPER+SHIFT+?` 

While the cheat-sheet can be overwhelming at first, it takes no more than maybe half an hour to get used the essentials: 

* `SUPER+SPACE`: Open an application.
* `SUPER+ENTER`: Open new terminal window.
* `SUPER+1...0`: Move to workspace 1...10. (i.e. virtual desktops)
* `SUPER+ARROW`: Change window focus.
* `SUPER+SHIFT+ARROW`: Change the position of current window.
* `SUPER+SHIFT+1...0`: Move current window to workspace 1...10.
* `SUPER+SHIFT+F`: Toggle between tiled mode and floating (stacking) mode. (useful for GUI apps that don't behave nicely in tiled mode.)

Knowing how to use the scratchpad is also useful. It's a hidden 11th workspace that you can access as a floating window from any workspace. Scratchpad is useful for hiding apps from sight or having constant access to certain apps. 

* `SUPER+SHIFT+M`: Send current window to the scratchpad. 
* `SUPER+SHIFT+A`: Open scratchpad. Toggles between windows in the scratchpad. 

Regolith allows for controlling the computer purely through keybindings without ever touching a mouse. This, you'll see, is a common theme of this experiment. 

A final note about terminal multiplexers: Yes, [tmux](https://github.com/tmux/tmux/wiki) is amazing. However, since I already use a tiling window manager, a terminal multiplexer is not required. 

In upcoming posts, I will be writing about the bash shell, task management with taskwarrior, scheduling with khal, text editing with vim, document processing with latex, and many more topics. Stay tuned!
