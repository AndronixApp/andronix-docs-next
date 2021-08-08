---
title: Migrating to F-Droid
description: "Know about the recent repository changes of Termux and migration from Google
Play Store to F-Droid."
category: Termux
badge: "Termux"
position: 11
---

<alert type="warning">This guide only deals with devices running Android 7 and above. **Termux removed the support for
Android 6 and below starting 1st January 2021.**</alert>


## What are the recent changes made to Termux?

All Termux repositories previously hosted on JFrog Bintray are down since `1st May 2021`. It means that all repositories
hosted on `dl.bintray.com` domain are no longer available anymore. It is due to the recent withdrawal of the Bintray
hosting service by JFrog (more about
that [here](https://jfrog.com/blog/into-the-sunset-bintray-jcenter-gocenter-and-chartcenter/)).


> F-Droid houses the latest stable versions of Termux that are now **not released** on the Play Store. It is the reason that we should have the latest version from F-Droid installed.

#### Okay, but what is **F-Droid** you ask?

F-Droid is an installable catalog of FOSS (Free and Open Source Software) applications for the Android platform. In In
simpler terms, F-Droid is like the Play Store for open-sourced applications for Android.

#### Is it safe?

F-Droid is entirely open-sourced and has millions of eyes monitoring the source code of the apps submitted. It has
strict compliance for the app submissions, and a zero-tolerance for Google APIs. Please read [this section](/security/termux) regarding the safety of these binaries.

## How can I migrate?

There are two ways which you can use to migrate to the Termux published on the F-Droid Store.

### Integrated Method

<iframe width="560" height="315" src="https://www.youtube.com/embed/NOnS9_Nfx4A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<alert type="success">This is an easier and recommended way to install your Termux app.</alert>

Just follow along-

* Open Andronix, click on the hamburger icon at the top-left to show the side-drawer, and select the **Settings** option.
  
  <img src="/images/termux/drawer.png" alt="drawing" width="200"/>
  
* Scroll to the bottom to find the **Re-rerun Termux Setup**. Click on it.
  
  <img src="/images/termux/settings.png" alt="drawing" width="200"/>
  
* You will now see one of two screens depending on if you already have Termux installed on your device. Please continue with the appropriate section-

#### Termux Installed

* You already have termux installed, so that the app will ask you the source of your installation. Press-
  YES: If you have installed the Termux app from the F-Droid repository. The setup will skip the process and redirect you back.
  NO: If you have installed the Termux app from the Google Play Store. You will see the Uninstall button after clicking it.
  NOT SURE: If you are unsure about the source of installation or do not understand the question.  You will see the Uninstall button after clicking it.
  
  <img src="/images/termux/termux_1.png" alt="drawing" width="200"/>

* Now, if you chose NO or NOT SURE, let's continue and try to uninstall Termux now. Press the **Uninstall** section and click **OK** on the pop-up.

  <img src="/images/termux/uninstall.png" alt="drawing" width="200"/>  
  <img src="/images/termux/uninstalling.png" alt="drawing" width="200"/>  
     

* After its successful uninstallation, you will see a **Download** layout. Click it to begin downloading the Termux app from its F-Droid repository. Please read [this section](/security/termux) regarding the safety of the downloaded binaries.

   <img src="/images/termux/download.png" alt="drawing" width="200"/>
  
  <alert type="info">The download might take a while depending upon your internet connection. You can minimize Andronix in the meanwhile, and we will notify you when the download is complete.</alert>

* As soon as the download is complete, you _might_ see a layout to **Allow Installation** on the screen. You can ignore this step if you don't see this. But if you do, click on it and **turn ON the switch** stating _Allow from this source_, and navigate back.

   <img src="/images/termux/allow_permission.png" alt="drawing" width="200"/>
   <img src="/images/termux/allow_permission_switch.png" alt="drawing" width="200"/>

* You should now see the final step, the **Installation** layout. Press it to begin the installation of the Termux app and click **Install** on the pop-up/screen. Please wait for the installation to complete, and it's done!
  
  <img src="/images/termux/termux_2.png" alt="drawing" width="200"/>
  <img src="/images/termux/installing.png" alt="drawing" width="200"/>   

#### Termux Not Installed

* You will see a **Download** layout. Click it to begin downloading the Termux app from its F-Droid repository. Please read [this section](/security/termux) regarding the safety of the downloaded binaries.

   <img src="/images/termux/download.png" alt="drawing" width="200"/>

  <alert type="info">The download might take a while depending upon your internet connection. You can minimize Andronix in the meanwhile, and we will notify you when the download is complete.</alert>

* As soon as the download is complete, you _might_ see a layout to **Allow Installation** on the screen. You can ignore this step if you don't see this. But if you do, click on it and **turn ON the switch** stating _Allow from this source_, and navigate back.

   <img src="/images/termux/allow_permission.png" alt="drawing" width="200"/>
   <img src="/images/termux/allow_permission_switch.png" alt="drawing" width="200"/>

* You should now see the final step, the **Installation** layout. Press it to begin the installation of the Termux app and click **Install** on the pop-up/screen. Please wait for the installation to complete, and it's done!

  <img src="/images/termux/termux_2.png" alt="drawing" width="200"/>
  <img src="/images/termux/installing.png" alt="drawing" width="200"/>   


### Manual Method
If you haven't installed Termux via the F-Droid client or via directly downloading their APK file and installing it, the
chances are that you're still running the Google Play Store version. In that case, follow the instruction below.

* Uninstall the present installation of Termux

> This will remove all the distros and other data related to Termux that you might have but is a necessary step in order to avoid version conflict. If you want to back up your data, please follow [this guide](https://wiki.termux.com/wiki/Backing_up_Termux)

1. Visit https://f-droid.org/en/packages/com.termux/ and download the APK of the latest version of Termux.
   Alternatively, you can also download and install the F-Droid client to help you manage future updates and other
   stuff.

    <img src="https://media3.giphy.com/media/uDnGcPkWLNk9jAa4jD/giphy.gif?cid=5e2148861a099ac679dd9f40900f53f5286a8a0fd71ff82e&rid=giphy.gif&ct=g" />

   <alert type="warning">Android might give you a warning that files like these might harm your device; you can safely
   ignore that. That is a generic warning triggered whenever you download an executable or installable file from
   elsewhere than the Google Play Store.</alert>


2. Once you've downloaded the APK, the next step is to **Allow installation from Unknown Sources**.

3. Click on the downloaded file, and you might see a popup like the one shown below:

    <img src="/images/unknown_sources.png" alt="drawing" width="200"/>

   _If you don't see this warning, please skip to the next step_ but if you do, follow along.

   Click on the **Settings** options of the popup and **turn on** the radio button as shown below.

    <img src="/images/allow_unknown_sources_radio.png" alt="drawing" width="200"/>

   p.s., you might be running a different browser and not chrome.

   Hit back a few times until you see this dialog shown below.

    <img src="/images/install_termux.png" alt="drawing" width="200"/>

4. Just click on the **Install**, and that's it 🎉.

3. You're all done! If you're still facing issues downloading packages, you can update the mirror lists to your liking,
   taking help from this [guide here](https://github.com/termux/termux-app/issues/2067).





