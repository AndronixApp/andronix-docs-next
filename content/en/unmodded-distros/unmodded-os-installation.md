---
title: How to install an OS with Andronix?
description: "Learn how to install your favourite distro easily."
category: Installation
position: 3
---

<alert type="success">These instructions assume that you have **Andronix version 6.0 or beyond** installed on your
device.</alert>
<alert type="info">This is **not** a guide to install a **Modded OS**. Please read the next article from this for more information on that.</alert>


<iframe width="560" height="315" src="https://www.youtube.com/embed/XkL1B0arrbw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Installing your favorite distro is a breeze with Andronix. Please follow these simple steps mentioned below-

* After you open the Andronix app, you will have a catalog of logos of the distributions you can use on your device. Select the distribution you want to install.

  <img src="/images/dashboard.png" alt="drawing" width="200"/>

* An information page will now open up. It mentions the size of the distro before extraction, the ease of use of the distro, the current version of the distro, and a button labeled as **Proceed**. Click the button to Proceed.

  <img src="/images/distro_detail_screen.png" alt="drawing" width="200"/>
  
* Click "Install" on the sheet that appears from the bottom.

  <img src="/images/distro_install_uninstall_sheet.png" alt="drawing" width="200"/>

* After the previous step, a page would ask you for the GUI you would like to see.

  <img src="/images/gui_selection.png" alt="drawing" width="200"/>

* You can choose a **Desktop Environment** if you would like to use your mouse as well as your keyboard, or you've
little or no experience with Linux. More information[here](../desktop-environments/desktop-environments.md).

  <img src="/images/de_selection.png" alt="drawing" width="200"/>

* You can choose a **Window Manager** if you only want to use your keyboard to manage Windows and other OS-level tasks. These are pretty light and fast but do require some skill before getting productive. More
information [here](../window-managers/window-managers.md).

  <img src="/images/wm_selection.png" alt="drawing" width="200"/>

* If you don't want a Graphical User-interface, you can go ahead with the **Command Line Interface**. You'll have
a terminal, which is enough if you know what you're doing in your session.

<alert type="info">If you're confused in choosing one option, we would always recommend you to go with a Desktop Manager.</alert>

___

Based on your selection, please follow one of these following articles-

* [Desktop Environment](#desktop-environment)
* [Window Manager](#window-manager)
* [CLI](#desktop-env)

___

### Desktop Environment

Now that you've decided to go ahead with a desktop environment, let's select what desktop environment you would like to
install. You can read [this page of the documentation](/desktop-environments/desktop-environments) to know more
about different DE and then click on the one you would like to install.

### Window Manager

Window Managers it is. Now select what Window Manager you would like to install. You can read [this part of the documentation](/window-managers/window-managers) for more
information on window managers.

### CLI

Since you've chosen the Command Line Interface, there's no extra configuration required on your part. You may proceed to the instructions below.

___

We are close to being done with the selections in the Andronix app. The following screen should be the screen displaying
on your device right now if you have correctly followed all the instructions.

> Andronix app has copied a command to your clipboard automatically.

  <img src="/images/termux_screen.png" alt="drawing" width="200"/>

You will need to run/execute this command in Termux.

<alert type="warning">Please read this before proceeding to make sure that you're using a compatible version of Termux for the installation process. Make sure that you've followed this guide for [Migration to F-Droid](/termux/migrating-to-f-droid)</alert>

* Open the termux app and run the following command first ```pkg update```, this will ensure that you are running the latest packages. Now **long press to paste the copied command and then hit enter to run it**.

  <img src="/images/termux_pkg_up.png" alt="drawing" width="200"/>  

* The installation/downloading will take some time. Please leave the termux app running.
  <alert type="warning">Please read this article to disable battery optimization for Termux so that processes running inside Termux don't randomly terminate.</alert>
  
* You can now start the distro by typing the following command in termux (Please choose your distro and execute the respective command)-

  * Ubuntu 18 `./start-ubuntu.sh`
  * Ubuntu 20 `./start-ubuntu20.sh`
  * Debian `./start-debian.sh`
  * Manjaro `./start-manjaro.sh`
  * Arch Linux `./start-arch.sh`
  * Fedora `./start-fedora.sh`
  * Void `./start-void.sh`
  * Alpine `./start-alpine.sh`
  * Kali Linux `./start-kali.sh`
  
* If you see ```root@localhost``` in the shell, you have successfully started your distro.
* Lastly, you need to start the VNC server actually to display the distro. Follow the steps mentioned [here](/vnc/vnc-basics).
