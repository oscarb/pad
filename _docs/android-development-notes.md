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

`onCreate` -> `onStart` -> `onResume`

`onPause` -> `onStop` -> `onDestroy`

`onPause` -> `onResume`

`onPause` -> `onStop` -> `onRestart` -> `onStart` 



## Loader

* Use loaders to avoid recreating asynct tasks between config changes

* [ud851-Exercises/MainActivity.java at T05b.02-Solution-AddAsyncTaskLoader · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/blob/T05b.02-Solution-AddAsyncTaskLoader/app/src/main/java/com/example/android/asynctaskloader/MainActivity.java)
* [Leveraging Loaders in Github Query - YouTube](https://www.youtube.com/watch?v=5o7SN8Z3VWs)

* Cache data so loader won't start ehen user navigates away from activity
https://github.com/udacity/ud851-Exercises/blob/T05b.03-Solution-PolishAsyncTask/app/src/main/java/com/example/android/asynctaskloader/MainActivity.java

* [Comparing S05.01-Exercise-AsyncTaskLoader...S05.01-Solution-AsyncTaskLoader · udacity/ud851-Sunshine](https://github.com/udacity/ud851-Sunshine/compare/S05.01-Exercise-AsyncTaskLoader...S05.01-Solution-AsyncTaskLoader)

## Persistance

* onSavedInstance
* SharedPreferences
* SQLLite Db
* File
* Server

### Preferences

* Use PreferenceFragment instead of Preference Activity
* [Make a PreferenceFragment - YouTube](https://www.youtube.com/watch?v=AFCywvOnM2M)
* [Comparing T06.02-Exercise-MakeAPreferenceFragment...T06.02-Solution-MakeAPreferenceFragment · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/compare/T06.02-Exercise-MakeAPreferenceFragment...T06.02-Solution-MakeAPreferenceFragment)

Reading From SharedPreferences
* `getDefaultSharedPreferences` : Gets a SharedPreferences instance that points to the default file that is used by the preference framework in the given context!
* `getSharedPreferences`: Gets a specific SharedPreferences instance by name in case you have more than one preference in the same context!

Preference Change Listener
* Don't forget to unregister in onDestroy
* `SharedPreferenceChangeListener` is triggered after any value is saved to the SharedPreferences file.
* `PreferenceChangeListener` is triggered before a value is saved to the SharedPreferences file. Because of this, it can prevent an invalid update to a preference. PreferenceChangeListeners are also attached to a single preference.

Update preference fragment
* [Preference Summary - YouTube](https://www.youtube.com/watch?v=cXqgkDC8fNg)
* [Comparing T06.08-Exercise-PreferenceSummary...T06.08-Solution-PreferenceSummary · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/compare/T06.08-Exercise-PreferenceSummary...T06.08-Solution-PreferenceSummary)

* [Settings - Patterns - Material design guidelines](https://material.io/guidelines/patterns/settings.html#settings-placement)

Should it be a setting?

![Make it a setting?](https://d17h27t6h515a5.cloudfront.net/topher/2016/November/582a4eda_screen-shot-2016-11-14-at-3.55.51-pm/screen-shot-2016-11-14-at-3.55.51-pm.png)

### SQLLite Database

* [sql-sqlite-commands-cheat-sheet.pdf](https://d17h27t6h515a5.cloudfront.net/topher/2016/September/57ed880e_sql-sqlite-commands-cheat-sheet/sql-sqlite-commands-cheat-sheet.pdf)
* [SQL Tutorial](http://www.w3schools.com/sql/)

Create a database
https://github.com/udacity/ud851-Exercises/compare/T07.02-Exercise-CreateTheDatabase...T07.02-Solution-CreateTheDatabase

## Security 

Smartphone Secure Development Guidelines — ENISA
https://www.enisa.europa.eu/publications/smartphone-secure-development-guidelines-2016