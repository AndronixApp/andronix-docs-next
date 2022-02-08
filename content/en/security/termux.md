---
title: Termux Security
description: "Is Termux secure?"
category: Security
position: 9
---

<alert type="success">
The current release of Termux is v0.118 </alert>

Since Termux ended support for the Google Play Store, Andronix 6.0 provides you with an easier way to install it on your Android device without even needing to leave the app.

Termux now uses the [F-Droid Store](https://fdroid.org) to host and build its app binaries. Downloading directly from
F-Droid is easy, but we decided to integrate the process into the Andronix app. Here are the following reasons because of which we do this-

1. F-Droid is an amazing FOSS store, but sadly it's slow. To counter this, we copy the latest and tested releases of Termux from their F-Droid repository to our [GitHub repository](https://github.com/AndronixApp/termux-releases).

2. This integrated process also helps eradicate the errors or flagging of the APK files downloaded typically from F-Droid.

## Is this safe?

Termux has to build the APK binary/file on F-Droid, which is under the eyes of millions of developers. So both Termux and F-Droid Store are **open-sourced**.

### Same binaries?

While we copy the F-Droid binaries onto our GitHub repository, we do not change the actual file. Therefore, you can ensure that the file is unchanged by downloading and [calculating the MD5 checksum](https://knowledge.autodesk.com/search-result/caas/sfdcarticles/sfdcarticles/Checking-the-MD5-checksum-of-a-Downloaded-File.html).

#### MD5 Checksum

Following this, you will find the MD5 checksum of the latest release of Termux on our repository and the latest release of Termux on their F-Droid repository.

Andronix's Release MD5

```
bd3af0ad4bbe9def1d6bb2e189e1b4e5
```

Termux's Release MD5

```
bd3af0ad4bbe9def1d6bb2e189e1b4e5
```

#### VirusTotal Report

Following this, you will find the [VirusTotal](https://virustotal.com) reports of Termux's latest release on our GitHub repository.

Check the [report](https://www.virustotal.com/gui/file/822ac152bd7c2d9770b87c1feea03f22f2349a91b94481b268c739493a260f0b/detection)
