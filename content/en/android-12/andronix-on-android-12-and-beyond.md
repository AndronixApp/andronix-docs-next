---
title: Andronix on Android 12 and beyond
description: "Android 12 and the phantom process killer"
category: Android Compatibility
position: 2
---


<alert type="info">
This information is necessary only if you are running android 12 and above.</alert>

## Problem

Android 12 has added the mechanism to monitor forked child processes started by apps and kills them if more than the
default 32 are found running. In simpler words Android now monitors the number of child process which are spawned by a
particular app and if in any case it exceeds the number of permitted processes, it just kills them.

This has lead to a lot of power apps like Termux, Tasker, Andronix, Debian NoRoot, being broken on Android 12 and 12L
devices.
There is nothing that can be done from our side since it's pushed in the Android's code.

### More Information

Issue on Termux's Repository:
[Android 12 Phantom Processes Killed (Process completed (signal 9) - press Enter)](https://github.com/termux/termux-app/issues/2366)

<alert type="success">
The good thing being that Google will include a fix/toggle for this (phantom process killing) in Android 12L or 13.
</alert>

[More information on the proposed solution](https://www.xda-developers.com/android-13-phantom-process-toggle)


<alert type="warning">
The aforementioned statement about the fix being included in the upcoming versions of Android might not be true for skinned Android ROMs like Samsung's OneUI, Xiaomi's MIUI, Oppo's ColorOS etc.
</alert>

## Solutions

Please follow the instructions given below for your respective Android versions.

### Fix for Android 12L and beyond

<alert type="info">
This fix might not work on your device as OEM often have the choice to exclude changes pushed by Google to the Android Open-Source Project at their will.
</alert>

Please follow the steps mentioned below to turn off the Phantom process killer-

1. We will first enable the **Developer Options** from the settings. To enable the same, please navigate to *Settings>
   About* Phone and find the **Build Number**.
   <img src="/images/android-12-fix/1.jpeg" alt="drawing" width="200"/>
   <img src="/images/android-12-fix/2.jpeg" alt="drawing" width="200"/>
2. Now tap it repeatedly until you see a toast notification along the lines of *You are now x steps away from being a
   developer*.
   <img src="/images/android-12-fix/3.jpeg" alt="drawing" width="200"/>
3. You might be asked to authenticate yourself, please do the same and then proceed.
   <img src="/images/android-12-fix/4.jpeg" alt="drawing" width="200"/>
4. Now, navigate to *Settings>System>Developer Options*. Enable the Developer Options on the next screen.
   <img src="/images/android-12-fix/5.jpeg" alt="drawing" width="200"/>
5. Find the section named **Feature Flags**, enter via clicking it.
   <img src="/images/android-12-fix/6.jpeg" alt="drawing" width="200"/>
6. Find the switch to turn off **settings_enable_monitor_phantom_procs**.
   <img src="/images/android-12-fix/7.jpeg" alt="drawing" width="200"/>

7. You are now all set! ✅

### Fix for Android 12

If you cannot upgrade to Android 12L or 13. Please try the following fix for Android 12-

1. Make sure you have the Android Debug Bridge (ADB) installed on your other device. You can
   follow [this guide on XDA developers](https://www.xda-developers.com/install-adb-windows-macos-linux/) to install ADB
   on Windows, macOS, or Linux.
2. After the installation, confirm if you have your device connected via ADB
   ```bash
   adb devices
   ```
3. You should see your device listed in the output of the above command. Now run the following command in the ADB shell
   ```bash
   adb shell /system/bin/device_config put activity_manager max_phantom_processes 2147483647
   ```
4. You should be all set! ✅˚

<br>
<br>
Credits for the discovery of the issue and the solution-

[agnostic-apollo](https://github.com/agnostic-apollo)










