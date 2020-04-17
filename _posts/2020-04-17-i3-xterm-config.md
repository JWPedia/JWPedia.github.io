---
layout: post
title: Configuring i3 Window Manager and XTerm | Living in the Command Line
permalink: /i3-xterm-config/
categories: technology minimalism
date: 2020-04-17
---

In my previous [post](cli-regolith), I talked about how I use an i3-based tiling window manager for a terminal-based workflow. A great thing about i3 and XTerm, my terminal emulator of choice, is their customizability. These are some preliminary configurations I made for improved quality of life. 

# XTerm's appearance in ~/.Xresources

The ~/.Xresources file customizes terminal emulators' appearance. As I use XTerm instead of URXVT, I first deleted all lines specific to URXVT. 

I increased the font size from 12 to 15 such that my eyes don't bleed all day:

```
xterm*faceName: Monospace
xterm*faceSize: 15
```

![Xterm theming](/Media/xterm_theme.png)

I made some customizations to the color scheme. These lines set the terminal as true color mode, and make it look like the screenshot.  

```
xterm*termName: xterm-256color

xterm*foreground: #d0d0d0
xterm*background: #272822

xterm*color0: #303030
xterm*color1: #d0d0d0
xterm*color2: #66AA11
xterm*color3: #c47f2c
xterm*color4: #30309b
xterm*color5: #7e40a5
xterm*color6: #3579A8
xterm*color7: #9999AA
xterm*color8: #303030
xterm*color9: #ff0090
xterm*color10: #80FF00
xterm*color11: #ffba68
xterm*color12: #5f5fee
xterm*color13: #bb88dd
xterm*color14: #4eb4fa
xterm*color15: #d0d0d0

xterm*boldMode: true

xterm*pointerColor: white
xterm*pointerColorBackground: black
xterm*cursorColor: yellow
xterm*cursorBlink: true
```

# Terminal QoL

Adding the following line in ~/.inputrc will make directory and file autocompletion case insensitive. It's nice to not have to remember whether some files start with uppercase or lowercase!

```
set completion-ignore-case on
```

These are some terminal aliases stored in ~/.bashrc I can't live without: 

```
# Displays subdirectories and files in list form, with human-redable file size, including hidden files
alias ll="lls -lha" 

# Displays weather forecast in metric, meters per second (wind velocity), and in narrow formatting
alias wttr="curl wttr.in/?mMn

# Use neovim as the default text editor instead of vim or vi
alias vim="nvim"
alias vi="nvim"

# Use htop as the default process monitor instead of top
alias top="htop"

# Update all packages in Ubuntu-based distros
alias upup="sudo apt-get upgrade && sudo apt-get update"

# Update all packages in arch-based distros
alias pacup="sudo pacman -Syu"
```

# Configuring i3 Window Manager

The configurations for i3 is stored in ~.i3/config and is easily modifiable by reading the comments and documentation. 

I made xterm the default terminal instead of urxvt:

```
bindsym $mod+Return exec xterm # Launch xterm instead of urxvt via keybinding
bindsym $mod+Ctrl+b exec xterm -e 'bmenu' # Launch bmenu in xterm instead of urxvt
bindsym $mod+F5 exec xterm 'cmus' # Make cmus in xterm the default music player
bindsym $mod+F6 exec xterm 'ranger' # Launch ranger file manager from xterm
```

I made firefox the default web browser:
```
bindsym $mod+F2 exec firefox
```

i3 uses jkl; keys for navigation by default. I changed them to the vim-style hjkl keybindings:

```
# Change focus
bindsym $mod+h focus left
bindsym $mod+j focus down
bindsym $mod+k focus up
bindsym $mod+l focus right

# Move focused window
bindsym $mod+Shift+h move left
bindsym $mod+Shift+j move down
bindsym $mod+Shift+k move up
bindsym $mod+Shift+l move right
```

This may be an unpopular choice, but I removed all workspaces escept workspace two and the scratchpad. This helps me stay focused without having lots of applications in the background, fragmenting my attention. I would, of course, create more workspaces on a laptop or a multi-monitor setup.  

```
set $ws1 1
set $ws2 2

bindsym $mod+1 workspace $ws1
bindsym $mod+Ctrl+1 move container to workspace $ws1
bindsym $mod+Shift+1 move container to workspace $ws1; workspace $ws1

bindsym $mod+2 workspace $ws2
bindsym $mod+Ctrl+2 move container to workspace $ws2
bindsym $mod+Shift+2 move container to workspace $ws2; workspace $ws2
```

I removed pamac-manager (install applications) and pcmanfm (file browser) from opening in floating mode by commenting these lines:

```
# for_window [class="application name here"] floating enable
```

I removed all gaps in between workspaces to maximize screen real-estate:

```
gaps inner 0
gaps outer 0
```

I increased the time it takes for the screen to autolock from 10 minutes to 2 hours:

```
exec --no-startup-id xautolock -time 120 -locker blurlock
```

I made some programs automatically start when i3 launches:

```
# ibus language input choice UI
exec_always ibus-daemon -drx --panel /usr/lib/ibus/ibus-ui-gtk3

# pcloud client for syncing files to local drive
exec_always pcloud
```
