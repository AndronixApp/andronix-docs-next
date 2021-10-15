---
title: FAQs
description: "The most commonly asked questions regarding Andronix with their solutions."
category: Frequently Asked Questions
badge: "FAQs"
position: 12
---

The most commonly asked questions regarding Andronix with their solutions.

### Getting this error whenever I try to install any OS

<img src="https://cdn.discordapp.com/attachments/840108865533902860/840110358252748810/Screenshot_2021-05-06-08-27-29-489_com.termux2.jpg" alt="drawing" width="200"/>

**Ans.** Termux app from the Play Store has been discontinued. Please follow [this guide](/termux/migrating-to-f-droid)

### Kali Linux errors out during installation.

**Ans.** We are aware of the current issues with Kali. It will be fixed soon but there's no ETA. Please consider using
any other distro like Debian.

### Modded Manjaro gives repository errors whenever I try to install or update any package.

**Ans.** Follow [this guide](https://forum.andronix.app/t/modded-manjaro-easy-setup-commands/), and you'll be good to
go.

### AlgGr not working on VNC

<img src="/images/faq/altgr.png" alt="drawing" width="200"/>

**Ans.** You can use [bVNC](https://play.google.com/store/apps/details?id=com.iiordanov.freebVNC) instead of [RealVNC](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android) and selected the highlighted option from the top menu. If that does not work either, please consider using [Android VNC](https://play.google.com/store/apps/details?id=android.androidVNC&hl)

### Vnc can’t open- usage: vncserver <display> error

<img src="/images/faq/vncError.png" alt="drawing" width="400"/>

**Ans.** Most of the users face this error whilst using Modded Manjaro. Here is the fix-
Please run this inside the Manjaro shell- 

```bash
sudo pacman -S wget tar sed --noconfirm && wget https://raw.githubusercontent.com/AndronixApp/AndronixOrigin/master/Pacman/tigervnc-fix.sh && sudo bash tigervnc-fix.sh
```
### Ubuntu 20.04: Firefox shows Gah. Your tab just crashed

Here's an easy fix for this error-
1. Enter about:config in address bar
2. Click “Accept the risk and continue”
3. Click “Show all”
4. Search for sandbox
5. Change first two values to false, and change security.sandbox.content.level to 1, exactly as in this picture:
   <img src="/images/faq/firefox.png" alt="drawing" width="500"/>
6. Restart Firefox.




