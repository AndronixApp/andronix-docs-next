---
title: Important Things
description: 'Please read this page before you start to use anything that Andronix
offers.' 
position: 1
category: Introduction
---

<!-- <img src="/preview.png" class="light-img" width="1280" height="640" alt=""/>
<img src="/preview-dark.png" class="dark-img" width="1280" height="640" alt=""/>
 -->
 
Many users out there are looking for a viable resource to use Linux system on their Android devices without rooting
their devices. Andronix is a viable option for these purposes but with some limitations. We make our best efforts to
provide a full Linux PC 💻experience to our users, but some things are just out of our hand due to certain restrictions
imposed by the Android layer, it's the SELinux 🔐 policies, and the process we use to run the Linux on the Android
devices.

On this page you can find the summary of what Andronix is not capable of doing with the reasons. So here is the list:

## Gaming

* Andronix is not capable of running **STEAM 🎮,** any PC games or emulate architecture using Wine/PlayOnLinux on any of
  its Linux systems. The main reason for this is because Steam is only made for Intel/AMD based CPU's and not mobile
  based CPU's i.e. aarch64, armv8, arm64, arm, armv7, arm32 etc.

## Architectural Limitations

* Andronix is not capable of running any software except software complied for **arm64/armv8/aarch64** architecture if
  you are using any **Android device** based of **Android 7** or above and has **arm64/armv8/aarch64** chipset. You can
  check your device architecture by using [**CPUZ**](https://play.google.com/store/apps/details?id=com.cpuid.cpu_z). If
  you are using any device which has Android layer such as **Chromebook** then Andronix will only be able to run
  software made for your architecture which may be **i386/i686/x86 or x86\_64.**

## PRoot Limitations

* Andronix does not claim that it will run all the software even if the software complies to all the conditions
  mentioned in the above point. If the software is made in such a way that it requires the presence of Linux Kernel or
  any hardware support which is not present in the ⚠ **PRoot environment** then the software might fail to run**.**
  Andronix uses PRoot environment which has certain inevitable limitations leading to unusable software.

## Development Environments

* Andronix is not made for compiling large chunks of code 👩💻such as building an Android app, any software or compiling
  kernels. Code compilations sometimes require specific hardware which is not present in PRoot environment which may
  lead to errors while compiling code. Any such reports on any support channel will not be entertained.

## Hacking

* The Linux environment made available by Andronix cannot be used for **hacking/cracking purposes** i.e. Wi-Fi hacking,
  packet capture etc. All these things require real hardware which supports all the features like packet capturing which
  is not available natively in Android phones.

## Hardware Limitations

* The Linux environment cannot mount/read any hardware such as drives or adapters 🖨. This is because fuse mount cannot
  be used under PRoot.


* Any Linux OS cannot be installed on External Storage as Android does not give permission to write on External storage
  such as sdcard or USB devices.


## Container Applications

* **SNAP/Docker/Flatpak** packages cannot be installed on any Linux environment. It is mainly due to two reasons.
  Primary being that both require kernel and bus modules which are unavailable in PRoot environment and second being
  that both are mainly focused on Intel/AMD based architectures and not for arm architecture.

  
## Networking and Init Systems

* You can't use any services such as VPN or anything which changes the properties of network cause the network used
  within Linux container is managed by Android and not Linux itself and hence it does not have access to modify any
  property of the network.

## Hardware acceleration

* Any available distro is **not Hardware Accelerated**. It's because Termux doesn't have hardware acceleration support.
  The day termux adds hardware acceleration to their app we will support it too. For any more queries regarding hardware
  acceleration proceed [here](https://gitter.im/termux/termux).



# How does this work?

Andronix is simple inside the hood \(well not really, but most of it is simple to understand\). Andronix uses **PRoot**
to run your favourite Linux distribution on your Android devices.

### What is PRoot?

According to the official PRoot documentation

> PRoot is a user-space implementation of **chroot, mount --bind, and binfmt\_misc**. This means that users don't need any privileges or setup to do things like using an arbitrary directory as the new root file system, making files accessible somewhere else in the file system hierarchy, or executing programs built for another CPU architecture transparently through QEMU user-mode.

or in easier words, the benefits of enabling PRoot include running Linux operating systems in a
Termux [chroot](https://en.m.wikipedia.org/wiki/Chroot) on an Android smartphone, tablet and Chromebook.

We use **Termux** to provide the command line, and the packages that are especially compiled for Termux implemented
inside Andronix.

## Are we open-source? 📖🔓

Yes but no. Andronix is partially open-source. All the free distro tar files, and the shell scripts are available on
our [GitHub repository](https://github.com/andronixapp). While all the paid things, like the actual Android app and all
the files concerning Andronix Modded OS are close-source for obvious reasons.

That doesn't mean that we don't love open-source, **we** ❤**open-source**. In fact if you're a developer or a maintainer
of an open-source project, **we will be more than happy to provide you everything for free** for life. Just get-in touch
with us and complete the process of verification😊. 
