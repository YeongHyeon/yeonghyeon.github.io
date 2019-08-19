---
layout: post
categories: posts
title: Remote Desktop Protocol Setup for Ubuntu
tags: [setting]
date-string: AUGUST 19, 2019
---

This post covers how to set up the remote desktop protocol for connecting Ubuntu. This method does not need a physical monitor for using GUI. VNC viewer can be basically used for connection but it needs physical monitor attachment.

### 1. Install 'XRDP' and 'Xfce Desktop Environment'
``` sh
sudo apt-get update   
sudo apt-get install xrdp

sudo apt-get install xfce4
```

### 2. Add Xfce session to '.xsession' and initialize 'XDRP'
``` sh
echo xfce4-session > ~/.xsession
sudo service xrdp restart
```

### 3. Connect remote PC via remote desktop application

<a href="https://apps.apple.com/us/app/microsoft-remote-desktop-10/id1295203466?mt=12">Microsoft Remote Desktop App</a>
