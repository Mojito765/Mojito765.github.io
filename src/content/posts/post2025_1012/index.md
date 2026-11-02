---

title: 'Install custom ROM on Xperia XZ1'
published: 2025-10-12
description: 'Commonly Used Commands.'
image: './xz1.jpg'
tags: [Guides]
category: 'Mobile'
draft: false
---

> Cover image source: [Xperia XZ1の特徴（スペック・機能）価格まとめ！](https://www.nicosuma.com/magazine/xperia-xz1-spec)

## Prerequisites

Before you start:
- Install [Android SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools)
- Confirm your model is Sony Xperia XZ1 **(G8341 / G8342 / G8343)**
- Enable USB Debugging
- Unlock the bootloader
- Backup


## Process log

Install [TWRP](https://twrp.me/Devices/Sony/).
```markdown
adb reboot bootloader
```

```markdown
fastboot flash recovery YOURTWRP.img
```

```markdown
fastboot reboot
```

Install a Custom ROM via TWRP (ADB Sideload Method).
```markdown
adb devices
```

```markdown
adb sideload YOURROM.zip
```

## Useful ADB and Fastboot Commands

_(Compiled and explained by [ChatGPT](https://chatgpt.com/))_

Below are some commonly used commands that can help during the flashing or troubleshooting process.
```markdown
📱 ADB Commands
- `adb devices` — Lists all connected devices recognized by ADB
- `adb reboot bootloader` — Reboots the device into Fastboot mode
- `adb sideload <filename>.zip` — Installs a ROM or update package via ADB sideload
- `adb push <local> <remote>` — Transfers a file from your computer to the device
- `adb pull <remote> <local>` — Copies a file from the device to your computer
  ⚡ Fastboot Commands
- `fastboot devices` — Lists devices connected in Fastboot mode
- `fastboot flash recovery twrp.img` — Flashes a custom recovery (e.g., TWRP)
- `fastboot boot twrp.img` — Temporarily boots into TWRP without flashing it
- `fastboot flash boot boot.img` — Flashes the boot image
- `fastboot reboot` — Reboots the device normally
  💡 Tip
  Always verify your device connection with `adb devices` or `fastboot devices` before running any flash commands.
```

## ROM_PixelExperience Plus

XDA Link: [[13][UNOFFICIAL] PixelExperience Plus [11-11-2023]](https://xdaforums.com/t/13-unofficial-pixelexperience-plus-11-11-2023.4509165/)

Build author/Device maintainer: Tux111

**Source code**
::github{repo="whatawurst/android_device_sony_poplar"}

**Source code**
::github{repo="PixelExperience/wiki"}

**Kernel**
::github{repo="whatawurst/android_kernel_sony_msm8998"}
