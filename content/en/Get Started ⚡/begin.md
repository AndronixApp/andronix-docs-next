---
title: Get Started
description: "Get started with using Andronix."
position: 2
badge: "Installation"
category: Introduction
---

<alert type="warning">This is a getting started guide only for Andronix 6.0 and above. For older docs visit [here](https://docs.andronix.app).</alert>

Andronix is designed to be as simple and intuitive as possible. Let's get started with the outline of the process here.

# UnModded OS

1. Install Andronix and launch it. After you have opened Andronix, you'll see all the different distros you can select to install.
2. Select the distro you would like to install click on the install icon.
3. You will now be presented with three options. Select one.
   - **Desktop Environments** - Gives you a GUI to interact with. More info [here.](../desktop-environment/desktop-managers)
   - **Window Managers** - Use your keyboard to manage windows. More info [here.](../window-managers/windows-managers)
   - **No GUI** - Work just from a command line and with no GUI at all.
4. After you have selected the aforementioned option. Please select the sub-category like desktop env like _XFCE_ or a window manager like _awesome_.
5. Now that you have selected all the things necessary, you should see a **command copied** splash screen.
6. You will have to open/install **[Termux](https://termux.com)**. Wait for it to initialize in it's first launch if you're installing it for the first time.
7. Andronix should have copied a command in the _step 5_. Paste this inside termux and press enter to run the command.
8. Wait for everything to complete.
   <alert type="warning">This part can take something from **20 minutes to more than an hour** depending upon your device. Please be patient.</alert>
9. After you see something like `Please launch the distro with...sh`. It's all ready to go.
10. Time to play a little with **VNC**. VNC allows you to connect to a server to actually see things happening on your screen since there is no actual display cable or HDMI attached to display it physically.
11. Start the distro with `start-{distro}.sh` where the distro stands for the distro you're installing. Here's the list of the start commands -<!-- todo add these -->
    - Ubuntu 18 -
    - Ubuntu 19 -
    - Ubuntu 20 -
    - Debian -
    - Alpine -
    - Arch -
    - Fedora -
    - Manjaro -
    - Void -
    - Kali -
12. After you type in one of the aforementioned commands, you'll see that the left side of the terminal has changed from `$` to `root@localhost`. If you get an error, please post ask about it on our [Discord Server](https://chat.andronix.app).
13. Now just type in `vncserver-start` and boom! almost everything done.

14. Now you can connect to your distro using any device as long as it is on your local network i.e. the network to which your phone is connected to like the same Wi-Fi. [Follow this guide for the process of connecting your device.](./vnc)



# Modded OS

<alert type="info">Modded OS are a paid product. The purchase is one-time and for life with unlimited install over indefinite devices.</alert>

Modded OS are pretty straight forward to install. Let's go through the process once.

1. Install Andronix and launch it. After you have opened Andronix, you'll see a button labelled as **Andronix Modded OS** click it and you'll see all the Modded OS you can buy/install.

2. After you have selected the Modded OS you want to install, you can now purchase it if you haven't or just install it, if you already own it. We'll assume that you have already bought your favourite distro.

3. You will now see an install and an uninstall button. Click on the button which says install and proceed.

4. The app will generate a token that will help you to download the Modded OS. After that you'll be redirected to the Termux screen.

5. Andronix should have copied a command in the _step 5_. Paste this inside termux and press enter to run the command.
6. Wait for everything to complete.
   <alert type="warning">This part can take something from **20 minutes to more than a couple of hours** depending upon your device. Please be patient.</alert>
7. After you see something like `Please launch the distro with...sh`. It's all ready to go.

8. Time to play a little with **VNC**. VNC allows you to connect to a server to actually see things happening on your screen since there is no actual display cable or HDMI attached to display it physically.
11. Start the distro with `start-{distro}.sh` where the distro stands for the distro you're installing. Here's the list of the start commands -<!-- todo add these -->
    - Ubuntu XFCE -
    - Ubuntu KDE -
    - Debian XFCE -
    - Manjaro XFCE -
    
9. After you type in one of the aforementioned commands, you'll see that the left side of the terminal has changed from `$` to `root@localhost`. If you get an error, please post ask about it on our [Discord Server](https://chat.andronix.app).
10. Now just type in `vncserver-start` and boom! almost everything done.

11. Now you can connect to your distro using any device as long as it is on your local network i.e. the network to which your phone is connected to like the same Wi-Fi. [Follow this guide for the process of connecting your device.](./vnc)
