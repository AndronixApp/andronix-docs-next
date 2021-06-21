---
title: XSDL Basics
description: "Learn how operate XSDL"
category: XSDL
position: 9
---

It is a X Window System / X11 server for Android. X11 servers are generally faster when compared to VNC but XSDL lacks
the beautiful UI which a VNC Viewer might have. It comes to your choice and what suits you the most.

## How to start a XSDL server?

* Download and install the XSDL app from Play Store
* Open XSDL and wait until you see something similar to the screenshot below
* Now start OS and type the command inside the distro's shell-

```bash
export DISPLAY=127.0.0.1:0 && bash ~/.vnc/xstartup &
```

If you are on a Wi-Fi network and want to access XSDL from other devices then change the command to :

```bash
export DISPLAY=192.168.0.100:0 && bash ~/.vnc/xstartup &
```