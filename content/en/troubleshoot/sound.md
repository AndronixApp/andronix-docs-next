---
title: Sound
description: "Learn how to output the sound from your Linux environment to the speakers of
your device."
category: Troubleshoot
---

You can use your speakers while using your distro to get all that excellent music from Spotify (or anything) while you code. We use Pulse Audio to get that sound out of the PRoot container to your phone's speakers.

<alert type="info">Modded OS have sound output through phone's speakers enabled out of the box.</alert>

Just follow these steps correctly in order to have sound output enabled-

* Close the distro if you have it opened with running exit inside Termux. _Ignore this step if you haven't had your distro running in the first place_.
```bash
exit
```
* Run the following command in **Termux (Not inside Linux)**
```bash
 pkg install wget && wget https://andronixos.sfo2.cdn.digitaloceanspaces.com/OS-Files/setup-audio.sh && chmod +x setup-audio.sh && ./setup-audio.sh
```
* Start the PulseAudio Server
```
pulseaudio --start
```

