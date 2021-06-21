---
title: IDEs (Development Environments)
description: "Learn how to install IDEs like IntelliJ, VS code and more."
category: Software
position: 13
---

We love to code here and Andronix is a portable computer. Why not use it to code anywhere? You can use full-fledged IDEs
inside Andronix.

<alert type="warning">We have only tested VS code, IntelliJ Idea, IntelliJ DataGrip, MonoDevelop (tested GTKsharp, ASP
NET, ASP NETCORE this last have a problem with the target framework), Mono (In console, you can compile simple console
programs in C #) Net Core. You can test other IDEs and edit this page to add it to the list.</alert>

## IntelliJ Idea

Here are the steps needed to install IntelliJ Idea on your Andronix instance

<alert type="info">This assumes that you have the SDK for your language already installed for the distro you are
using.</alert>

* Download the latest tar.gz file from JetBrains
  official [download page](https://www.jetbrains.com/idea/download/#section=linux).
* After downloading the tar.gz, make sure that it is in your download folder and after run the following command.
  Change `x` to the name of the tar downloaded.

```bash
tar -xzf ideaIU-2xxx.x.x.tar.gz -C ~/Desktop/
```

* The tar should now be unzipped in `Desktop/ideaIU-2xxx.x.x`, where 'x' stands for the year and version number.
* Now choose the command from below and run it inside Linux terminal

### Debian/ Ubuntu/ Kali Linux

```bash
sudo apt install openjdk-11-jdk -y
```

### Arch/Manjaro

```bash
sudo pacman -S jdk-openjdk
```

### Void Linux:

```bash
xbps-install -S openjdk
```

### Alpine:

```bash
apk --no-cache add openjdk11 --repository=http://dl-cdn.alpinelinux.org/alpine/edge/community
```

### Fedora:

<alert type="warning">
Fedora is not recommended for use of Jetbrains IDE.
</alert>

* We can now proceed to run Idea, navigate to Desktop/ideaIU-2xxx.x.x/bin and execute the idea.sh with the following
  command-

```bash
./idea.sh
```

* Yay! 🎊 That's all you need to do to run IntelliJ on your device.

## VS Code

<alert type="info">Andronix supports VS Code on all four of our support CPU architectures namely ARM64(armv8), armv7,
i686 and x86_64.</alert>

<alert type="success">Modded OS come installed with VS Code of out the box.</alert>

### Debian based distros (Package Manager - apt)

Please execute the following command from within the distro's shell-

```bash
apt install wget -y && wget https://raw.githubusercontent.com/AndronixApp/AndronixOrigin/master/Uninstall/vscode_patch.sh && chmod +x vscode_patch.sh && ./vscode_patch.sh
```