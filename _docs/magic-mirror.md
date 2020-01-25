---
title: Magic Mirror
tags:
  - android
  - hardware
published: true
---

# Magic Mirror

## Installation

### Ports

Local Port | Container Port | Type
-----------|----------------|-------
8775 | 8080 | TCP

### Volume

File/folder | Mount path | Type
------------|------------|--------
apps/magic-mirror/css/custom.css | /opt/magic_mirror/css/custom.css
apps/magic-mirror/modules | /opt/magicmirror/modules
apps/magic-mirror/config | /opt/magic-mirror/config

### Network

bridge


### Start


```
docker run --name magic-mirror \
    -p 8775:8080 \
    --env TZ=Europe/Stockholm
    -v /volume1/apps/magic-mirror/css/custom.css:/opt/magic_mirror/css/custom.css \
    -v /volume1/apps/magic-mirror/modules:/opt/magic_mirror/modules \
    -v /volume1/apps/magic-mirror/config:/opt/magic_mirror/config \
    -v /etc/localtime:/etc/localtime:ro \
    -d xbgmsharp/docker-magicmirror
```


## Android 

Apps: 
* [These Are The Android apps You Can Use for Your Magic Mirror](https://www.magicmirrorcentral.com/android-app-magic-mirror/)

### Guide

* [HannahMitt/HomeMirror: Android application powering the mirror in my house](https://github.com/HannahMitt/HomeMirror)
* [DIY Magic Mirror Android Edition - Updated April '17: 6 Steps (with Pictures)](http://www.instructables.com/id/Magic-Mirror-Mini-Android-Powered/)
* [Overview | Android Smart Home Mirror | Adafruit Learning System](https://learn.adafruit.com/android-smart-home-mirror)
* [My Bathroom Mirror Is Smarter Than Yours – Medium](https://medium.com/@maxbraun/my-bathroom-mirror-is-smarter-than-yours-94b21c6671ba)
* [Build your own Android magic mirror on the cheap - SlashGear](https://www.slashgear.com/build-your-own-magic-mirror-on-the-cheap-03425380/)
* [Android Motion Sensing Smart Mirror: 4 Steps (with Pictures)](http://www.instructables.com/id/Android-Motion-Sensing-Smart-Mirror/)
* [Android Powered Magic Mirror | Dan The IOT Man](https://dantheiotman.com/2017/08/29/android-powered-magic-mirror/)
* [Magic Mirror for the Masses - Album on Imgur](https://imgur.com/gallery/DsXyt)

## Screen

* [Xonay Labs | Michael Teeuw](http://michaelteeuw.nl/post/81059936176/magic-mirror-part-ii-the-monitor)
