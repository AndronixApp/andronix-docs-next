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

Installing your favourite distro is a breeze with Andronix. Please follow these simple steps mentioned below-

## 1. Preparation 🚀
* After you open the Andronix app, you will find the option to install a **Linux Distribution**. Click the card.
  <img src="/images/install_new/install_dashboard.jpg" alt="drawing" width="200"/>

* Now, you will see all the distributions that can be installed on your Android device.
  <img src="/images/install_new/install_distro_selection.jpg" alt="drawing" width="200"/>


## 2. Selection ⭐️
* Click on the distro that you would like to install.

  <alert type="warning">We recommend you to get started with **Ubuntu** if you are overwhelmed by the options.</alert>

* Here comes the **GUI Selection**
  <img src="/images/install_new/install_gui_selection.jpg" alt="drawing" width="200"/>
  <alert type="info">Graphical User Interface or GUI is the visual interface that you interact with to do things in your Linux distribution.</alert>
* You now have the option to choose among the three following options:
  1. **Desktop Environment**: You can choose a Desktop Environment if you would like to use your mouse as well as your keyboard, or you've little or no experience with Linux. More information [here](../desktop-environments/desktop-environments.md).
  2. **Window Manager**: You can choose a Window Manager if you only want to use your keyboard to manage Windows and other OS-level tasks. These are pretty light and fast, but do require some skill before getting productive. More
     information [here](../window-managers/window-managers.md)
  3. **Command Line Interface (CLI)**: If you don't want a Graphical User-interface, you can go ahead with the **Command Line Interface**. You'll have a terminal, which is enough if you know what you're doing in your session.

  <alert type="info">If you're confused in choosing one option, we would always recommend you to go with a Desktop Manager.</alert>




* Based on your selection above, please follow the respective instructions below:

  #### Desktop Environment

  Now that you've decided to go ahead with a desktop environment, let's select what desktop environment you would like to
  install. You can read [this page of the documentation](/desktop-environments/desktop-environments) to know more
  about different DE and then click on the one you would like to install.
  <img src="/images/install_new/install_de_selection.jpg" alt="drawing" width="200"/>

  #### Window Manager

  Window Managers it is. Now select what Window Manager you would like to install. You can read [this part of the documentation](/window-managers/window-managers) for more information on window managers.
  <img src="/images/install_new/install_wm_selection.jpg" alt="drawing" width="200"/>

  #### CLI

  Since you've chosen the Command Line Interface, there's no extra configuration required on your part. You may proceed to the instructions below.


## 3. Termux Execution 💻
Now comes the part where the actual installation of your Linux distribution begins.
<alert type="success">Andronix app has copied a command to your clipboard automatically. </alert>

  <img src="/images/install_new/install_termux_exec.jpg" alt="drawing" width="200"/>

* You will need to run/execute this command in Termux.

<alert type="warning">Please read this before proceeding to make sure that you're using a compatible version of Termux for the installation process. Make sure that you've followed this guide for [Migration to F-Droid](/termux/migrating-to-f-droid)</alert>

* Open the Termux app and **long press to paste the copied command and then hit enter to run it**.

  <img src="/images/termux_pkg_up.png" alt="drawing" width="200"/>  

* The installation/downloading will take some time. Please leave the Termux app running.
  <alert type="warning">Please read this article to disable battery optimization for Termux so that processes running inside Termux don't randomly terminate.</alert>
  <alert type="info">If the installation appears to be stuck on a certain step for an unusual time, please press the **Enter** key to resume the execution.</alert>


* Now, click the **Command Executed** button at the bottom of the screen.
* After the script has been executed successfully, Click the **Execution Finished** button at the bottom.
  <img src="/images/install_new/install_script_exec.jpg" alt="drawing" width="200"/>

## 4. Starting Distribution ⚡️

<alert type="info">If you are already in the distro shell i.e. you see `root@localhost` mentioned on Termux. Please skip the next section.</alert>

* You can now start the distro by typing the following command in Termux (Please choose your distro and execute the respective command) and running it-

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

## 5. VNC Configuration 📺

* In order for you to actually interact with the installed distribution's GUI, we will need to set up a VNC server.
* Andronix has already copied the necessary command on your clipboard. Just paste it in Termux (in the Distro shell _[root@localhost]_) and execute it.

  <img src="/images/install_new/install_start_vnc.jpg" alt="drawing" width="200"/>

* If you're prompted to select a resolution, just press **Enter** to dynamically select the resolution.
* That's it. Now install the [RealVNC app](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android) from the Google Play Store (or any other VNC client).
* Now press the **Add(+)** button to add a VNC connection. Enter _localhost:1_ as the address and give it a name. Save the record.
* Click the newly created VNC address, and you are all done! ✅

  <img src="/images/install_new/install_complete.jpg" alt="drawing" width="200"/>


