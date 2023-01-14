---
title: VNC Basics
description: "Learn how operate a VNC server."
category: VNC
position: 8
---

## Operating the VNC Server

Let's learn how to operate VNC servers including starting, stopping and debugging them.

### Starting a VNC server

* Andronix has already copied the necessary command on your clipboard if you are on the VNC server page. Just paste it in Termux (in the Distro
  shell _[root@localhost]_) and execute it
    ```bash
    vncserver-start
  ````

    <img src="/images/install_new/vnc_server_start_command.jpg" alt="drawing" width="200"/>
    

* If you're prompted to select a resolution, just press **Enter** to dynamically select the resolution.
* That's it. Now install the [RealVNC app](https://play.google.com/store/apps/details?id=com.realvnc.viewer.android)
  from the Google Play Store (or any other VNC client).

    <img src="/images/install_new/real_vnc_connection_add.jpg" alt="drawing" width="200"/>

* Now press the **Add(+)** button to add a VNC connection. Enter _localhost:1_ as the address and give it a name. Save
  the record.

    <img src="/images/install_new/real_vnc_connection_input.jpg" alt="drawing" width="200"/>

* Click the newly created VNC address

    <img src="/images/install_new/real_vnc_connection_selection.jpg" alt="drawing" width="200"/>


* You might be warned that the connection is untrusted. Click **OK** to continue.

    <img src="/images/install_new/vnc_unencrypted_connection.jpg" alt="drawing" width="200"/>

* You will be prompted to enter a password. Enter the password you set while installing the distro step and click **
  Continue**.

    <img src="/images/install_new/real_vnc_password_input.jpg" alt="drawing" width="200"/>
    <alert type="info">You can turn "Remember the password" toggle on for your convenience.</alert>
* You will now be able to see the GUI of your Linux distribution.

    <img src="/images/install_new/real_vnc_first_connection.jpg" alt="drawing" width="200"/>
* You might notice the horrible picture quality. Don't worry, we'll fix that in the next step.
* Press the **i** button on the top menu bar of the VNC app to open the settings.

  <img src="/images/install_new/real_vnc_i_button.jpg" alt="drawing" width="200"/>

* You will see the settings of the VNC app. Scroll down to the **Picture Quality** section and select **High**.

    <img src="/images/install_new/real_vnc_picture_quality_settings.jpg" alt="drawing" width="200"/>

* Now, you will be able to see the GUI of your Linux distribution in high quality.

    <img src="/images/install_new/real_vnc_all_done.jpg" alt="drawing" width="200"/>

* You can now use your Linux distribution as you would on a PC ✅.

    <img src="/images/install_new/install_complete.jpg" alt="drawing" width="200"/>


<alert type="warning">Always remember to **Stop the VNC** server before exiting the distro.</alert>

### Stopping a VNC server

It is necessary to stop the VNC server once you are done using your distro or exiting it. To stop the VNC server execute the following command in the distro shell-

```bash
vncserver-stop
```

Once you execute it, the terminal will ask you for a port number. Enter **1** as the port number and click enter.

## VNC Settings

<alert type="info">These instructions assume that you have started your distro and are inside the distro shell (not a
Termux shell).</alert>

### Setting a desired resolution

To apply your desired resolution, please execute the following command-

```bash
nano /usr/local/bin/vncserver-start
```

Now, you just need to change the last line of this file to-

```bash
vncserver -name remote-desktop -geometry 1920x1080 :1
```

<alert type="info">You can replace the 1920x1080 to your desired resolution.</alert>

Since you've made changes to the file, let's save it by pressing `ctrl + x` , then hit y and finally hit `Enter`.

### How to change resolution permanently in Modded OS /Ubuntu 19

To change resolution permanently execute the following command in the distro's shell-

```bash
nano /usr/local/bin/vnc
```

Once you do this, replace the second line with-

```bash
LD_PRELOAD=/lib/aarch64-linux-gnu/libgcc_s.so.1 vncserver -localhost no -depth 24 -name remote-desktop -geometry 1920x1080 :$PORT
```

<alert type="info">You can replace the 1920x1080 to your desired resolution and then restart/start the VNC
Server.</alert>

Once you are done, just press `Ctrl+X` and then type `Y` and then hit enter. Now when you'll do just choose the first
option i.e., **Start vnc-server with autodetect/dynamic resolution**.

### How to change the picture quality in VNC

If you are using bVNC then you do not need to make any changes. It will make it's required changes itself.

If you are using RealVNC Viewer, then connect to the VNC Server and then click on _(i)_ button at the top. Change
Picture Quality to **High**, or to your desired quality.

## VNC on other devices

<alert type="success">You can access the instance running on your phone on any other device on your network.</alert>

Continuing with the instructions, please make sure that both of your devices are sharing the same network. If you don't
have access to Wi-Fi, you can start the hotspot from the device having the Linux installed and connect the other device
to the hotspot. Once both the devices are under the same network, execute the following command inside the distro's
shell-

```bash
nano /usr/local/bin/vncserver-start
```

Now edit the last line and change it to-

```bash
vncserver -name remote-desktop -geometry 1920x1080 -localhost no :1
```

<alert type="warning">If you are using an Arch-based distribution like Manjaro or Arch Linux itself, please execute the
following command instead of the command as mentioned earlier-</alert>

```bash
vncserver -name remote-desktop -geometry 1920x1080 -localhost :1
```

Once you are done with this open a new Termux session (drag from the left to open the sidebar for more options) and
type:

```
ip a
```

Now copy then **WLAN IP** address (eg. _192.168.xx.xx_). Now use this IP Address on the other device with the port
number as 1 (eg. _192.168.xx.xx:1_ ).  