---
title: SSH Basics 
description: "Learn how operate an SSH server."
category: SSH
position: 8
---

We recommend that you use SSH Server from Termux instead of using in a Linux environment. Using an SSH Server from
Termux gives you control of both your device and your Linux OS. We are providing you both the methods for the same down
below-

## SSH via Termux

You can follow [this](https://glow.li/technology/2015/11/06/run-an-ssh-server-on-your-android-with-termux/) link to get
to know the process of using SSH from Termux. This tutorial is provided officially by one of Termux developers.

## SSH via Linux

Since Linux is executed by using PRoot, it cannot override the default configurations of the Android connectivity, so
the port number needs to be changed. Follow the below steps to use SSH from Termux:

Install **openSSH** inside Linux. Choose the command for your distro accordingly from the given list:

### Ubuntu 19

```bash
apt install openssh-server nano -y
```

### Ubuntu 18

```bash
apt install openssh-server nano -y
```

### Kali Linux

```bash
apt install openssh-server nano -y
```

### Debian

```bash
apt install openssh-server nano -y
```

### Manjaro

```bash
pacman -S openssh nano --noconfim
```

### Arch

```bash
pacman -S openssh nano --noconfim
```

### Fedora

```bash
dnf install -y openssh-server nano
```

### Alpine

```bash
apk add openssh-server nano
```

### Void

```bash
xbps-install openssh nano
```

* Once OpenSSH server is installed on your Linux system, we need to modify some things to make it accessible in network
  escaping Android limitations. Now execute-

```
nano /etc/ssh/sshd_config 
```

* Find and change the line `#Port 22` to `Port 2222`
* Find the line `#PermitRootLogin prohibit-password`  or `#PermitRootLogin yes` and change it to `PermitRootLogin yes` .
  If it is already `PermitRootLogin yes` then you do not need to change anything.
* Now when you are done with all the above steps press `CTRL+X` and then type `Y` and then press `Enter`
* Now do `ssh-keygen -A` and then `ssh-keygen`
* Now we need to set password first. To set password type `passwd` and set any password.
* Once this process is complete, just run `/usr/sbin/sshd` to start the SSH server.
* Now just type `ip a` and copy the IP Address of `wlan` and to connect to SSH Server.
* To connect to SSH server type `ssh root@localhost -p 2222` and use the password to connect to the server.  