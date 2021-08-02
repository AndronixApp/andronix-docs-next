---
title: Browsers
description: "Learn how to use your favourite browsers with Andronix"
category: Software
position: 12
---

<alert type="warning">If you are having any **armv7** based device, browsers might fail to work due to unknown reasons.</alert>

<alert type="info">These instructions assume that you have started your distro and are inside the distro shell (not a
Termux shell).</alert>

## Firefox

Please follow the following instruction (in accordance to the distro you're running) to install Firefox-

### Ubuntu 19/ Ubuntu 20/ Debian/ Kali Linux

```bash
apt install firefox-esr -y
```

### Arch / Manjaro

```bash
pacman -S firefox --noconfirm
```

### Void Linux

```bash
xbps-install -S firefox
```

### Alpine

```bash
Sadly Alpine does not provide Firefox support for ARM devices as or now.
```

## Chromium
Please follow the following instruction (in accordance to the distro you're running) to install Chromium-

### Ubuntu / Ubuntu 19 / Debian / Kali Linux

```bash
wget https://raw.githubusercontent.com/AndronixApp/AndronixOrigin/master/Uninstall/ubchromiumfix.sh && bash ubchromiumfix.sh

```

<alert type="info">If the Chromium does not launch from Application Menu then try the following command inside VNC
terminal:

* chromium --no-sandbox
* chromium-browser --no-sandbox
</alert>

### Arch / Manjaro

```bash
pacman -S chromium --noconfirm
```

### Void Linux

```
Sadly chromium is not available for Void Linux.
```

### Alpine

```bash
apk add chromium
```

### Fedora

```bash
dnf install chromium 
```
