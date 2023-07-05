---
title: Android Device Guide
tags:
  - android
  - apps
  - mobile
published: true
---

# Android Device Guide

## New device setup

### Before factory reset 

* Backup WhatsApp database
* Close tabs in Kiwi browser
* Backup photos to external storage
* Create new BankID using old BankID
* Sign into Keybase using old device


### After factory reset
* Go through settings
* Set up quick tiles
* Add extensions in Kiwi Browser
* Go through apps one by one
* Add Tasker permissions

### Tasker setup

#### Quick tiles

1. Keep Display On
2. Home Control

#### Global variables

#### Home screen widgets

* TV Remote

#### Permissions

**React to long volume press**
```
adb shell pm grant net.dinglisch.android.taskerm android.permission.SET_VOLUME_KEY_LONG_PRESS_LISTENER
```

**Listen to/write changes in secure settings**
```
adb shell pm grant net.dinglisch.android.taskerm android.permission.WRITE_SECURE_SETTINGS
```

**Read logs**
```
adb shell pm grant net.dinglisch.android.taskerm android.permission.READ_LOGS
```

## What to backup when formatting?


* Beamed files`
* Documents
* Screenshots




## Apps priority

### Top Priority
* [bankid](https://play.google.com/store/apps/details?id=com.bankid.bus)
* [Google Calendar](https://play.google.com/store/apps/details?id=com.google.android.calendar)
* [Chrome Beta](https://play.google.com/store/apps/details?id=com.chrome.beta)
* [Messenger](https://play.google.com/store/apps/details?id=com.google.android.apps.messaging)
* [Nova Launcher Prime](https://play.google.com/store/apps/details?id=com.teslacoilsw.launcher.prime)
* [SMS Backup +](https://play.google.com/store/apps/details?id=com.zegoggles.smssync)
* [Swype Keyboard](https://play.google.com/store/apps/details?id=com.nuance.swype.dtc)
* [WhatsApp Messenger](https://play.google.com/store/apps/details?id=com.whatsapp)


### High priority

* [Contacts](https://play.google.com/store/apps/details?id=com.google.android.contacts)
* [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm)

### Medium priority

* [AlmostTI - TI Calc Emulator](https://play.google.com/store/apps/details?id=com.fms.ati)


## Root Samsung Galaxy Tab S2 9.7 SM-T813 (gts210vewifi)

### Requirements

* Charge device
* Enable USB debugging
* Enable OEM unlock
* Install [Samsung Drivers](https://developer.samsung.com/galaxy/others/android-usb-driver-for-windows) on Windows
* Download and install [Odin 3.10.7](https://forum.xda-developers.com/showthread.php?t=2711451)
* Download latest stable [Magisk](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445) 
* Download [Forced Encryption Disabler](https://www.dropbox.com/s/dy6434a5w32d9sl/Tabs3_oreo_forced%2Bencryption_disabler.zip?dl=1)
* Download [TWRP](https://www.dropbox.com/s/x319tpsyh6s7mh1/samsung_sm-t813_gts210vewifixx_nougat_twrp.tar?dl=1) [mirror](https://eu.dl.twrp.me/gts210vewifi/)


### Instructions

1. Turn off device
2. Hold *Volume Down* + *Home* + *Power* to enter download mode
3. Connect device to computer 
4. Press *Volume up* to continue
5. Launch Odin and verify that `added` appears in the log
6. Click the AP button and browse for TWRP
7. In options, enable F. Reset Time is enabled and Re-Partition and Auto-Reboot is disabled
8. Press start 

### Reset to original firmware

Get original firmware using [SamFirm](https://forum.xda-developers.com/galaxy-tab-s/general/tool-samfirm-samsung-firmware-t2988647) or from https://updato.com/firmware-archive-select-model/

1. Enter download mode on tablet 
2. In Odin, click AP and select the unzipped firmware file
3. Wait
4. Click start
5. Wait
6. If necessary, reboot into recovery mode and factory reset, then wait again

[Source](https://android.stackexchange.com/questions/176786/samsung-galaxy-tab-s2-in-bootloop-standard-recovery-not-working)
