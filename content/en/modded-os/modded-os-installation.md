---
title: How to install Modded OS?
description: "Learn how to install your favourite Modded OS easily."
category: Modded OS
position: 4
---

Installing Modded OS is a very simple process. Here's how to get started quickly-

<alert type="info">You are allotted a set number of downloads that are allowed in a day and in a month. This is a very
generous limit and shouldn't be hit by most users, but we can always help you increase it for a valid use case. This is
strictly done to curb down the abuse of the downloading system. **You can see this limit on the OS information page of
each distribution.**</alert>

That information aside, we can begin installing the distro now. Follow the steps below-

1. Open the app and click on the Modded OS button on the dashboard. After you get into the Modded OS section, you'll see
   the various distros that you can install.
2. Click the distro that you already own or are willing to buy. If you haven't already paid for it in the past, the app
   will show you the price and other information that you can refer and make the purchase. As soon as you complete the
   purchase, you can follow the next set of instructions.
   <alert type="success">For more information on in-app purchases and commerce on the Andronix app, refer
   to [this section]().</alert>

3. Now that we have the distro linked to our profile, we can continue. You would see 3 buttons, one labelled "Install"
   , "Uninstall" and "Download Quota".

4. As we are installing the distro, we will click on **Install**. The app will now communicate to our servers and
   generate a script command with some parameters. **The app would have copied the command to your clipboard
   automatically.**

5. Just open Termux (make sure you've read this [Migration to F-Droid](../Termux/migrating-to-f-droid.md)) and paste the
   command by long pressing and selecting "Paste". Hit the return/enter button to execute the command.

6. Wait for the installation to complete. The time taken will depend on the hardware of the device and your internet
   connection.

<alert type="info">You might notice unusual low speeds while downloading the distro tar file. You can ignore it because
the file is simultaneously extracted while it's getting downloaded and hence the process is slow.</alert>

___________________

After the installation has completed, and you don't see any errors at the end, we've made it to the last part,
configuring your installed distro! Now you just need to **start the distro**.

You can start the distro with typing the following command in termux (Please choose your distro and execute the
respective command)-

* Ubuntu XFCE `./start-<>.sh`
* Ubuntu KDE `./start-<>.sh`
* Debian XFCE `./start-<>.sh`
* Manjaro XFCE `./start-<>.sh`
  This will start the post-installation process i.e., setting up the essential packages. You will need to wait until
  this finishes.

8. If the post-installation setup successfully executed, you will see a **blue screen** asking for a username. You can
   choose any username unless that's a reserved keyword like admin, root etc. (your name works fine). Press **Enter** to
   proceed. <alert type="info">If you can't access your keyboard for entering the username, press the ESC key at the
   bottom. This restarts the script and this time make sure that you have your keyboard out (click anywhere on the
   terminal) when you're in the Termux shell.</alert>

9. After the username, it's time to set up a password. You can choose any password as long as it is longer than 6
   characters. Press Enter to proceed. Confirm the password by re-entering it and press enter to continue.

10. Now you need a Root Password. You can choose any password as long as it is longer than 6 characters. Press Enter to
    proceed. Confirm the root password by re-entering it and press enter to continue.

11. The next screen will show all the information entered. Check if those are the correct passwords and username (if
    not, press esc or back button to restart the script). Press Enter to proceed.

12. Now, wait until the system is creating the user. You should see something like this while the system is setting-up
    the user.

13. That's it! After this finishes, you will see- ```{your_username}@localhost:~$```

[comment]: <> (Add a link to VNC article)


Lastly, start the VNC server (want to know what is a VNC server? Read more [here]()) with executing the following
command **inside the distribution shell** and not the Termux shell - ```vncserver-start```

_To make sure you're executing it inside the distribution, please start the distro first before starting the VNC
server._



