---
title: Android Studio
tags:
  - android
published: true
---

# Android Studio

[Download Android Studio and SDK Tools](https://developer.android.com/studio/index.html)

## Themes

* [Color Themes](http://color-themes.com/?view=index)
  * [OceanSunset](http://color-themes.com/?view=theme&id=563a1a8e80b4acf11273aed1)

## Plugins

* Markdown support
* .ignore
* Key Promoter
* CodeGlance

## Virtual devices

Use x86 images instead of x86_64, for faster boot-up of emulator

* Nexus 5 API 24
  * Android 7.0 x86_64

### Install 

File > Import settings...

* HAXM 
* Enable USB debugging on device



## Code style

* [Google](https://github.com/google/styleguide/blob/gh-pages/intellij-java-google-style.xml)
* [Square](https://github.com/square/java-code-styles)

## Settings

* Mouse: Change font size (zoom) with Ctrl + Mouse Wheel
* Font: Consolas 12px
* Editor > General > Appearance: Show line numbers
* Editor > General > Appearance: Show method separators
* Auto import Java: Add unambiguous imports on the fly
* Optmize imports on the fly
* Prefer XML editor
* Remove file header comments _Created by Oscar on..._ 
* Editor > General > Code Completion > Autopopup documentation in (ms)
* Avoid stepping into `android.*` when [debuggning](http://stackoverflow.com/questions/19486163/android-studio-how-to-debug-through-my-code-only)

Setup horizontal scroll wheel to <kbd>Alt</kbd> + <kbd>←</kbd>/<kbd></kbd>

### Keyboard shortcuts

Shortcut | Action 
---------|--------
<kbd>Ctrl</kbd> + <kbd>NumPad +</kbd> | Increase Font Size 
<kbd>Ctrl</kbd> + <kbd>NumPad -</kbd> | Decrease Font Size 
<kbd>Ctrl</kbd> + <kbd>NumPad-0</kbd> | Reset Font Size 
<kbd>Ctrl</kbd> + <kbd>R</kbd> | Refactor This... 
<kbd>Ctrl</kbd> + <kbd>NumPad ,</kbd> | Run
<kbd>Alt</kbd> + <kbd>'</kbd> | VCS popup
<kbd>Ctrl</kbd> + <kbd>NumPad 1</kbd> | Toggle Presentation mode
<kbd>Ctrl</kbd> + <kbd>NumPad 2</kbd> | Toggle Distraction Free mode
<kbd>Ctrl</kbd> + <kbd>NumPad 3</kbd> | Toggle Full Screen mode



## Live Templates

### Create a new intent

Abbreviation
: Intnt

Description
: Create an intent that starts an Activity

Template text: 

```
android.content.Intent intent = new Intent(this, $className$.class);
intent.putExtra($CURSOR$);
startActivity(intent);
```

Reformat according to style

Template variables

Name | Expression | Default value | Skip if defined 
-----|------------|---------------|-----------------
className | classNameComplete() | | 
CURSOR | | | 

### Create a card


### Snackbar

## Tips

* Rename variable, method or class with <kbd>Shift</kbd> + <kbd>F6</kbd>
* Extend selections with <kbd>Alt</kbd> + <kbd>↑</kbd>
* Insert code snippets with <kbd>Ctrl</kbd> + <kbd>J</kbd>
* Move between methods with <kbd>Alt</kbd> + <kbd>↑</kbd>/<kbd>↓</kbd>
* Look into the body of a called method with <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>I</kbd>
* Select code and extract into a method with <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>M</kbd>
* View parameters of a method with <kbd>Ctrl</kbd> + <kbd>P</kbd>
* Evaluate expressions when debugging with <kbd>Alt</kbd> + <kbd>F8</kbd>
* Inspect variables while debugging by holding <kbd>Alt</kbd> while clicking on them
* Test regular expressions with Check RegExp
* Use <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Space</kbd> for smarter completion
* Find more tips with the Productivity Guide in the Help menu
* Display documentation with <kbd>Ctrl</kbd> + <kbd>Q</kbd>
* Select the next of selection with <kbd>Alt</kbd> + <kbd>J</kbd>
* Use scratches for keeping code temporarily 
* Use the `tools:` namespace in layout-files for previewing in Android Studio

When switching between a debug apk and a signed release apk on the same device, remember to first uninstall the debug apk _for all users_. 


Edit Custom VM options...
```
-Xms256m
-Xmx1024m
```

C:\Users\Oscar\.gradle\gradle.properties
```
org.gradle.daemon=true

org.gradle.jvmargs=-Xmx2048m -XX:MaxPermSize=512m -XX: +HeapDumpOnOutOfMemoryError -Dfile.encoding=UTF-8

org.gradle.parallel=true

org.gradle.configureondemand=true
```



### Resources

* Android Studio Tips Of the Day - Roundup #1 ([www.developerphil.com](http://www.developerphil.com/android-studio-tips-of-the-day-roundup-1/))
* (About) 10 Things You (Probably) Didn’t Know You Could do in Android Studio –  ([Google Developers – Medium](https://medium.com/google-developers/about-10-things-you-probably-didn-t-know-you-could-do-in-android-studio-de231071b375#.olspr5v48))
* Android Studio Tips and Tricks ([Michael Evans](http://michaelevans.org/blog/2016/01/06/android-studio-tips-and-tricks/))
* Tips & Tricks For App Development Using Android Studio ([TechNetExperts](http://www.technetexperts.com/mobile/tips-tricks-for-app-development-using-android-studio/))
* Things You May Not Know: Tools Attributes — ([Randomly Typing](http://www.randomlytyping.com/blog/2015/6/17/things-you-may-not-know-about-tools-attributes))
* 50 Android Studio Tips, Tricks & Resources you should be familiar with, as an Android Developer – Medium ([medium.com](https://medium.com/@mmbialas/50-android-studio-tips-tricks-resources-you-should-be-familiar-with-as-an-android-developer-af86e7cf56d2#.saghh212l))



## Resources
