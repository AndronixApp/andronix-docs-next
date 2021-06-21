---
title: Internal Storage
description: "Learn how to use your device's internal storage inside the Linux environment."
category: Troubleshoot
---

To mount internal storage you just need to run two commands.

* First open new Termux session (Swipe from left corner to right) and type:
```bash
termux-setup-storage
```
Now it will ask you for Storage permission. **Allow the Storage permission**.

* Once you are done with it type:

```bash
nano start-{distroname}.sh
```
<alert type="warning">Make sure to replace _{distroname}_ with your specific distro name.</alert>

* Now search for line:
```bash
#command+=" -b /sdcard"
```
* If you find this line, then remove it and change it to
```bash
command+=" -b /sdcard"
```
* If you don't find the line then add the above mentioned line as shown in the screenshot below.
//

* Once you are done with it press `Ctrl+X` and then press `Y` and then `Enter`. Now start your linux system and do `cd /` . Now you will be able to see a folder `sdcard` which means you have successfully mounted your Internal Storage.