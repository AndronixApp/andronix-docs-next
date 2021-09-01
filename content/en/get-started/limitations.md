---
title: Limitations of Andronix
description: 'Please read this page before you start to use anything that Andronix
offers.' 
position: 2 
category: Introduction
---

Many users out there are looking for a viable resource to use the Linux system on their Android devices without root their
devices. Andronix is a viable option for these purposes but with some limitations. We do our best to provide a complete
Linux PC 💻experience to our users, but some things are just out of our hands due to certain restrictions imposed by the
Android layer, it's the SELinux 🔐 policies, and the process we use to run the Linux on the Android devices.

On this page, you can find a summary of what Andronix can't do with the reasons. So here is the list:

## Gaming

Andronix cannot run **STEAM 🎮,** any PC games or emulate architecture using Wine/PlayOnLinux on any of its Linux
systems. The main reason for this is that Steam only supports Intel/AMD-based CPUs and not mobile-based CPUs, i.e.,
aarch64, armv8, arm64, arm, armv7, arm32, etc.

## Architectural Limitations

* Andronix cannot run any software except software complied for **arm64/armv8/aarch64** architecture if you are using any **Android device** based on **Android 7** or above and has **arm64/armv8/aarch64** chipset. You can check your device architecture by using [**CPUZ**](https://play.google.com/store/apps/details?id=com.cpuid.cpu_z). If you are using any Android layer device such as **Chromebook**, then Andronix will only run software made for your architecture, which may be **i386/i686/x86 or x86\_64.**

## PRoot Limitations

* Andronix does not claim that it will run all the software even if it complies with all the conditions mentioned above.
  If the said software requires Linux Kernel or any hardware support that is not present in the ⚠ **PRoot environment**,
  then the software might fail to run**.**
  Andronix uses PRoot environment, which has certain inevitable limitations leading to unusable software.

## Development Environments

* Andronix does not support compiling large chunks of code 👩💻such as building an Android app, any software, or compiling kernels. Code compilations sometimes require specific hardware not present in the PRoot environment, leading to errors while compiling code. Any such reports on any of the support channels won't be dealt with.

## Hacking

* You won't be able to use penetration testing tools for **hacking/cracking purposes**, i.e., Wi-Fi hacking, packet capture, etc. These things require real hardware that supports all the features like packet capturing, which is not available natively in Android phones.

## Hardware Limitations

* The Linux environment cannot mount/read any hardware such as drives or adapters 🖨. It is because the fuse mount
  cannot be used under PRoot.


* Any Linux OS cannot be installed on External Storage as Android does not permit to write on External storage such as SD-cards or USB devices.

## Container Applications

* **SNAP/Docker/Flatpak** packages cannot be installed on any Linux environment. The primary reason is that both require kernel and bus modules unavailable in the PRoot environment. The second is that both are mainly focused on
  Intel/AMD-based architectures and not on the ARM architecture.

## Networking and Init Systems

* You can't use any services such as VPN or anything which changes the properties of the network cause the network operated within the Linux container is managed by Android and not Linux itself. Hence, it does not have access to modify any property of the network.

## Hardware acceleration

* Any available distro is **not Hardware Accelerated**. It's because Termux doesn't have hardware acceleration support.
  The day termux adds hardware acceleration to their app, we will support it too. For any more queries regarding
  hardware acceleration, proceed [here](https://gitter.im/termux/termux).

# How does this work?

Andronix is simple inside the hood (well, not really, but most of it is simple to understand). Andronix uses **PRoot**
to run your favorite Linux distribution on your Android devices.

### What is PRoot?

According to the official PRoot documentation

> PRoot is a user-space implementation of **chroot, mount --bind, and binfmt\_misc**. This means that users don't need any privileges or set up to do things like using an arbitrary directory as the new root file system, making files accessible somewhere else in the file system hierarchy, or executing programs built for another CPU architecture transparently through QEMU user-mode.

or in easier words, the benefits of enabling PRoot include running Linux operating systems in a
Termux [chroot](https://en.m.wikipedia.org/wiki/Chroot) on an Android smartphone, tablet, and Chromebook.

We use **Termux** to provide the command line and the packages that are specially compiled for Termux implemented
inside Andronix.

## Are we open-source? 📖🔓

Yes, but no. Andronix is partially open-source. The free distro (.tar) files and the shell scripts are available on
our [GitHub repository](https://github.com/andronixapp). While all the paid things, like the actual Android app and all
the files concerning Andronix Modded OS, are closed-source for apparent reasons.

That doesn't mean that we don't love open-source, **we** ❤**open-source**. If you're a developer or a maintainer of an
open-source project, **we will be more than happy to provide you everything for free** for life. Just get in touch with
us and complete the process of verification😊. 
