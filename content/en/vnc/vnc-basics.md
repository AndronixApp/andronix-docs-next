---
title: VNC Basics
description: "Learn how operate a VNC server."
category: VNC
position: 8
---

## Operating the VNC Server

### Starting a VNC server

First you need to make sure that you have any Desktop Environment installed in your Linux OS. After you make sure that
you're inside the OS shell (shell you get after starting the distro) and not the Termux shell, execute the following
command in that-

```bash
vncserver-start
```

Now just download any VNC Viewer app from Play Store (eg. Real VNC, bVNC etc.) and connect to localhost:1 or the
configured port.

### Stopping a VNC server

It is necessary to stop VNC server once you are done with using your distro, or you are exiting it. To stop the VNC
Server execute the following command in the distro shell-

```bash
vncserver-stop
```

Once you execute it, terminal will ask you for a port number. Enter 1 as the port number and click enter.

## VNC Settings

<alert type="info">These instructions assume that you have started your distro and are inside the distro shell (not a
Termux shell).</alert>

### Setting a desired resolution

To apply your desired resolution, please execute the following command-

```bash
nano /usr/local/bin/vncserver-start
```

Now, you just need to change the last line of this file to-

```bash
vncserver -name remote-desktop -geometry 1920x1080 :1
```

<alert type="info">You can replace the 1920x1080 to your desired resolution.</alert>

Since you've made changes to the file, let's save it by pressing `ctrl + x` , then hit y and finally hit `Enter`.

### How to change resolution permanently in Modded OS /Ubuntu 19

To change resolution permanently execute the following command in the distro's shell-

```bash
nano /usr/local/bin/vnc
```

Once you do this, replace the second line with-

```bash
LD_PRELOAD=/lib/aarch64-linux-gnu/libgcc_s.so.1 vncserver -localhost no -depth 24 -name remote-desktop -geometry 1920x1080 :$PORT
```

<alert type="info">You can replace the 1920x1080 to your desired resolution and then restart/start the VNC
Server.</alert>

Once you are done, just press `Ctrl+X` and then type `Y` and then hit enter. Now when you'll do just choose the first
option i.e., **Start vnc-server with autodetect/dynamic resolution**.

### How to change the picture quality in VNC

If you are using bVNC then you do not need to make any changes. It will make it's required changes itself.

If you are using RealVNC Viewer, then connect to the VNC Server and then click on _(i)_ button at the top. Change
Picture Quality to **High**, or to your desired quality.

## VNC on other devices

<alert type="success">You can access the instance running on your phone on any other device on your network.</alert>

Continuing with the instructions, please make sure that both of your devices are sharing the same network. If you don't
have access to Wi-Fi you can start the hotspot from the device having the Linux installed and connect the other device
to the hotspot. Once your both the devices are under same network, execute the following command inside the distro's
shell-

```bash
nano /usr/local/bin/vncserver-start
```

Now edit the last line and change it to-

```bash
vncserver -name remote-desktop -geometry 1920x1080 -localhost no :1
```

<alert type="warning">If you are using a Arch based distribution like Manjaro or Arch Linux itself, please execute the
following command instead of the aforementioned command-</alert>

```bash
vncserver -name remote-desktop -geometry 1920x1080 -localhost :1
```

Once you are done with this open a new Termux session (drag from the left to open the sidebar for more options) and
type:

```
ip a
```

Now copy then **WLAN IP** address (eg. _192.168.xx.xx_). Now use this IP Address on the other device with the port
number as 1 (eg. _192.168.xx.xx:1_ ).  