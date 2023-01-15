---
title: How to install Modded OS?
description: "Learn how to install your favourite Modded OS easily."
category: Modded OS
position: 5
---

Installing Modded OS is a straightforward process. Here's how to get started quickly-
<alert type="info">You are allotted a set number of downloads that are allowed in a day and a month. It is a very
generous limit and shouldn't be hit by most users, but we can always help you increase it for a valid use case. It is
strictly done to curb down the abuse of the downloading system. **You can see this limit on the OS information page of
each distribution.**</alert>

<iframe width="560" height="315" src="https://www.youtube.com/embed/_3DdVI1jNtM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
That information aside, we can begin installing the distro now. Follow the steps below-

## 1. Preparation 🚀

* Open the Andronix app and click on the **Andronix Modded OS** card to proceed further.

* Open the app and click on the **Modded OS** button on the dashboard. After you get into the Modded OS section, you'll
  see the various distros that you can install.

    <img src="/images/modded_install_new/modded_distro_selection.jpg" alt="drawing" width="200"/>

* Click the distro that you already own or are willing to buy. If you haven't already paid for it in the past, the app
  will show you the price and other information that you can refer and make the purchase. As soon as you complete the
  purchase, you can follow the next set of instructions.

  **Unpaid Screen**
  <img src="/images/modded_install_new/modded_os_unpaid.jpg" alt="drawing" width="200"/>

  **Paid Screen**
  <img src="/images/modded_install_new/modded_distro_proceed.jpg" alt="drawing" width="200"/>

[comment]: <> (   <alert type="success">For more information on in-app purchases and commerce on the Andronix app, refer)

[comment]: <> (   to [this section]&#40;&#41;.</alert>)

* Now that we have the distro linked to our profile, we can continue.

## 2. Selection ⭐️

* You would see three buttons, one labeled **Install**, **Uninstall**, and **Download Quota**.

    <img src="/images/modded_install_new/modded_distro_options.jpg" alt="drawing" width="200"/>

* As we are installing the distro, we will click on **Install**.

## 3. Termux Execution 📥

Now comes the part where the actual installation of your Linux distribution begins.
<alert type="success">Andronix app has copied a command to your clipboard automatically. </alert>

   <img src="/images/modded_install_new/modded_termux_exec.jpg" alt="drawing" width="200"/>

* You will need to run/execute this command in Termux.

<alert type="warning">Please read this before proceeding to make sure that you're using a compatible version of Termux
for the installation process. Make sure that you've followed this guide
for [Migration to F-Droid](/termux/migrating-to-f-droid)</alert>

* Open the Termux app and **long press to paste the copied command and then hit enter to run it**.

  <img src="/images/modded_install_new/modded_os_command_termux.jpg" alt="drawing" width="200"/>  

    * The installation/downloading will take some time. Please leave the Termux app running.
      <alert type="warning">Please read this article to disable battery optimization for Termux so that processes
      running
      inside Termux don't randomly terminate.</alert>
      <alert type="info">You might notice unusual low speeds while downloading the distro tar file. You can ignore it
      because
      the file is simultaneously extracted while it's getting downloaded, and hence the process is slow.</alert>

* Now, click the **Command Executed** button at the bottom of the screen.
* After the script has been executed successfully, Click the **Execution Finished** button at the bottom.
  <img src="/images/install_new/install_script_exec.jpg" alt="drawing" width="200"/>

## 4. Starting Distribution ⚡️

After the installation has been completed, and you don't see any errors at the end, we've made it to the last part,
configuring your installed distro! Now you need to **start the distro**.

You can start the distro by typing the following command in termux (Please choose your distro and execute the
respective command)-

* Ubuntu XFCE `./start-andronix.sh`
* Ubuntu KDE `./start-androkde.sh`
* Debian XFCE `./start-androdebian.sh`
* Manjaro XFCE `./start-androjaro.sh`
  This will start the post-installation process i.e., setting up the essential packages. You will need to wait until
  this finishes.


* If the post-installation setup is successful, you will see a menu to select the region. You can use the **arrow
  keys** as shown in the screenshot below to move the selection and hit **ENTER** to proceed forward.

  <img src="/images/moddedos/modded_os_region_arrow_marker.png" alt="drawing" width="200"/>

* Once you have selected the region, you can choose your **City** in the following menu and proceed forward.

  <img src="/images/moddedos/modded_os_city.png" alt="drawing" width="200"/>

* Now you can select the keyboard layout if you have any specific layout other than the default English keyboard. We
  will go ahead with the English keyboard layout, so press **Enter** and proceed forward.

  <img src="/images/moddedos/modded_os_keyboard.png" alt="drawing" width="200"/>

* If everything goes perfectly, you will see a **blue screen** asking for a username. You can choose any username unless
  that's a reserved keyword like admin, root, etc. (your name works fine). Press **Enter** to
  proceed. <alert type="info">If you can't access your keyboard for entering the username, press the ESC key at the
  bottom. Again, it restarts the script and this time, make sure that you have your keyboard out (click anywhere on the
  terminal) when you're in the Termux shell.</alert>

  <img src="/images/username_user.png" alt="drawing" width="200"/>

* After the username, it's time to set up a password. You can choose any password as long as it is longer than 6
  characters. Press Enter to proceed. Confirm the password by re-entering it and press Enter to continue.

  <img src="/images/pass_user.png" alt="drawing" width="200"/>

* Now you need a Root Password. You can choose any password as long as it is longer than six characters. Press Enter to
  proceed. Confirm the root password by re-entering it and press Enter to continue.


* The next screen will show all the information entered. Check if those are the correct passwords and the username (if
  not,
  press the ESC or back button to restart the script). Press Enter to proceed.

  <img src="/images/confirm_user.png" alt="drawing" width="200"/>

* Now, wait until the system is creating the user. You should see something like this while the system is setting-up the
  user.

  <img src="/images/user_creation_moddedos.png" alt="drawing" width="200"/>

## 5. VNC Configuration 📺

<alert type="info">That's it! After this finishes, you will see- ```{your_username}@localhost:~$```</alert>

* Now the Start VNC server page should have opened

    <img src="/images/install_new/install_start_vnc.jpg" alt="drawing" width="200"/>

* In order for you to actually interact with the installed distribution's GUI, we will need to set up a VNC server.
* Follow this [comprehensive guide](/vnc/vnc-basics) to set up a VNC server and use your distro.



