---

title: Migrating to F-Droid
description: "Know about the recent repository changes of Termux and migration from Google Play Store to F-Droid."
category: Termux
badge: "Termux"
position: 11
---

<alert type="warning">This guide only deals with devices running Android 7 and above. **Termux removed the support for Android 6 and below starting 1st January 2021.**</alert>


## What are the recent changes made to Termux?

All Termux repositories previously hosted on JFrog Bintray are down since `1st May, 2021`. This means that all
repositories hosted on `dl.bintray.com` domain are no longer available anymore. This is due to the recent withdrawal of
the Bintray hosting service by JFrog (more about
that [here](https://jfrog.com/blog/into-the-sunset-bintray-jcenter-gocenter-and-chartcenter/)).

### What to do now?

There can now be the following scenarios

#### 1. I already have Termux installed on my device.

Since you already have termux installed, the next step will be detecting if it's the one from the Google Play Store or
F-Droid.

> F-Droid houses the latest stable versions of Termux that are now **not released** on the Play Store. This is the reason that we should have the latest version from F-Droid installed.

#### Okay, but what is **F-Droid** you ask?

F-Droid is an installable catalogue of FOSS (Free and Open Source Software) applications for the Android platform. In
simpler terms, F-Droid is like the Play Store for open sourced applications for Android.

#### Is it safe?

As said F-Droid is entirely open-sourced and has millions of eyes monitoring the source code of the apps submitted. It
has strict compliance for the app submissions, and a zero-tolerance for Google APIs.
___________________________
If you haven't installed Termux via the F-Droid client or via directly downloading their APK file and installing it,
chances are that you're still running the Google Play Store version. In that case follow the instruction below

* Uninstall the present installation of Termux

> This will remove all the distros and other data related to Termux that you might have but is a necessary step in order to avoid version conflict. If you want to backup your data, please follow [this guide](https://wiki.termux.com/wiki/Backing_up_Termux)

* Visit https://f-droid.org/en/packages/com.termux/ and download the APK of the latest version of Termux. Alternatively
  you can also download and install the F-Droid client to help you manage future updates and other stuff.
* You're all done! If you're still facing issues downloading packages you can update the mirror lists to your liking,
  taking help from this [guide here](https://github.com/termux/termux-app/issues/2067).




