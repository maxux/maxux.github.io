---
layout: post
title: UART on Raspberry Pi 3 and Pi Zero W
---

In order to have working /dev/ttyAMA0 on Raspberry Pi 3 and Pi Zero W, you need
to disable Bluetooth and enable uart. This works, even on new kernel (4.9+)

If you don't disable bluetooth, you'll have Kernel Panic during boot (bad PC value)

Update `config.txt` settings:
```
dtoverlay=pi3-disable-bt
enable_uart=1
```
