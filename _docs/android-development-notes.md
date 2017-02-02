---
title: Android Development Notes
tags:
  - android
published: true
---

# Android Development Notes

## `android:launchMode`

When up-navigation is present, use `singleTop` for the main activity to preserve state when navigating upwards.

See 
* [android:launchMode](https://developer.android.com/guide/topics/manifest/activity-element.html#lmode)
* [Tasks and Back Stack](https://developer.android.com/guide/components/activities/tasks-and-back-stack.html#TaskLaunchModes)
* [android - How can I return to a parent activity correctly?](http://stackoverflow.com/questions/12276027/how-can-i-return-to-a-parent-activity-correctly/15933890#15933890)

## compileSdkVersion, minSdkVersion, and targetSdkVersion

* [Picking your compileSdkVersion, minSdkVersion, targetSdkVersion](https://medium.com/google-developers/picking-your-compilesdkversion-minsdkversion-targetsdkversion-a098a0341ebd#.6xnsu03hg)


* [Please, don’t commit commented out code](https://medium.com/@kentcdodds/please-don-t-commit-commented-out-code-53d0b5b26d5f#.ju4jsavqz)

* Use tools to preview stuff, see https://developer.android.com/studio/write/tool-attributes.html
http://www.randomlytyping.com/blog/2015/6/17/things-you-may-not-know-about-tools-attributes

* [Android Project Structure — alternative way – Google Developers Experts – Medium](https://medium.com/google-developer-experts/android-project-structure-alternative-way-29ce766682f0#.h71ecd3x8)

## Lifecycle

* Use `onStop()` for when Android is killing the acitivity

## Loader

* Use loaders to avoid recreating asynct tasks between config changes

* [ud851-Exercises/MainActivity.java at T05b.02-Solution-AddAsyncTaskLoader · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/blob/T05b.02-Solution-AddAsyncTaskLoader/app/src/main/java/com/example/android/asynctaskloader/MainActivity.java)
* [Leveraging Loaders in Github Query - YouTube](https://www.youtube.com/watch?v=5o7SN8Z3VWs)

