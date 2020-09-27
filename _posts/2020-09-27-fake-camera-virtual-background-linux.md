---
layout: post
title: Fake camera with virtual background on Linux 
date: 2020-09-27 19:09:00
description: Using virtual camera background with Zoom and Teams on Linux
---
Zoom and Teams are supported by Linux. However, they provide limited functions, especially the limited virtual background function. For this purpose, I tested the following solution which works well on both Zoom and Teams, providing not only virtual background, but also foreground. 

The solution is based on the github repository of [Linux-Fake-Background-Webcam](https://github.com/fangfufu/Linux-Fake-Background-Webcam). This is based on the blog article of [Open Source Virtual Background](https://elder.dev/posts/open-source-virtual-background/). 

Installation is pretty clear to follow from the above website. To use it, I am taking a note here for personal purpose: 

```console
foo@bar:~$ cd /path/to/Linux-Fake-Background-Webcam
```

In one termal, 
```console
foo@bar:~$ cd bodypix
foo@bar:~$ node app.js
```

In another terminal,
```console
foo@bar:~$ cd fakecam
foo@bar:~$ python fake.py
```

I am using conda to setup the Python environment, as the default Python 3 is too old on my Linux (Ubuntu 16.04). So before running the above, I should run

```console
foo@bar:~$ conda activate    # I am using the base one (default one)
```

The background image and foreground (and foreground\_mask) can be replaced in the folder of fakecam. To activate the images, run ctrl + c in the fakecame console. To quit fakecam, run ctrl + \\. 

 
