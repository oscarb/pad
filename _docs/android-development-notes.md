---
title: Android Development Notes
tags:
  - android
published: true
---

# Android Development Notes

## `android:launchMode`

When up-navigation is present, use `singleTop` for the main activity to preserve state when navigating upwards. This will also stop new activites from being started from a notification.

See 
* [android:launchMode](https://developer.android.com/guide/topics/manifest/activity-element.html#lmode)
* [Tasks and Back Stack](https://developer.android.com/guide/components/activities/tasks-and-back-stack.html#TaskLaunchModes)
* [android - How can I return to a parent activity correctly?](http://stackoverflow.com/questions/12276027/how-can-i-return-to-a-parent-activity-correctly/15933890#15933890)

## Uri

Build Urls using [Uri.Builder](https://developer.android.com/reference/android/net/Uri.Builder.html)

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

![Lifecycle](https://i.stack.imgur.com/HNzS6.png)



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

## Content provider

[Example App](https://github.com/udacity/ud851-Exercises/tree/student/Lesson09-ToDo-List/T09.07-Solution-SwipeToDelete)

ud851-Exercises/Lesson08-Quiz-Example/T08.02-Exercise-AddAsyncTaskToRetrieveCursor at student · udacity/ud851-Exercises
https://github.com/udacity/ud851-Exercises/tree/student/Lesson08-Quiz-Example/T08.02-Exercise-AddAsyncTaskToRetrieveCursor

[Comparing S09.01-Exercise-ContentProviderFoundation...S09.01-Solution-ContentProviderFoundation · udacity/ud851-Sunshine](https://github.com/udacity/ud851-Sunshine/compare/S09.01-Exercise-ContentProviderFoundation...S09.01-Solution-ContentProviderFoundation)

[Comparing S09.04-Exercise-UsingCursorLoader...S09.04-Solution-UsingCursorLoader · udacity/ud851-Sunshine](https://github.com/udacity/ud851-Sunshine/compare/S09.04-Exercise-UsingCursorLoader...S09.04-Solution-UsingCursorLoader)

1. Get permission to use the ContentProvider.
	`<uses-permission android:name="com.example.appname.TERMS_READ" />
2. Get the ContentResolver
	```
    ContentResolver resolver = getContentResolver();
    Cursor cursor = resolver.query(Contract.CONTENT_URI, null, null, null, null);
    ``` 
3. Pick one of four basic actions on the data: query, insert, update, delete
4. Identify the data you are reading or manipulating to create a URI
5. In the case of reading from the ContentProvider, display the information in the UI


Creating a content provider
1. Extend the ContentProvider class and implement the required methods
2. Register it in the Manifest
3. Define URI's
4. Add URI's to the contract class
5- Build a URIMatcher to match URI patterns

Methods
query, insert, update, delete

URI
content://com.example.appname/specificData

CONTENT_URI

Cursor methods arguments

projection - filter columns
selection - how to filter rows
selection args - what to filter
sort order

Match integer: #
Match string: *

Example of `getType`:

```
public String getType(@NonNull Uri uri) {
    int match = sUriMatcher.match(uri);

    switch (match) {
        case TASKS:
            // directory
            return "vnd.android.cursor.dir" + "/" + TaskContract.AUTHORITY + "/" + TaskContract.PATH_TASKS;
        case TASK_WITH_ID:
            // single item type
            return "vnd.android.cursor.item" + "/" + TaskContract.AUTHORITY + "/" + TaskContract.PATH_TASKS;
        default:
            throw new UnsupportedOperationException("Unknown uri: " + uri);
    }
}
```

The best way to asynchronously load data from any ContentProvider is with a CursorLoader

[Comparing S09.05-Exercise-MoreDetails...S09.05-Solution-MoreDetails · udacity/ud851-Sunshine](https://github.com/udacity/ud851-Sunshine/compare/S09.05-Exercise-MoreDetails...S09.05-Solution-MoreDetails)


BulkInsert
[Comparing S09.02-Exercise-ContentProviderBulkInsert...S09.02-Solution-ContentProviderBulkInsert · udacity/ud851-Sunshine](https://github.com/udacity/ud851-Sunshine/compare/S09.02-Exercise-ContentProviderBulkInsert...S09.02-Solution-ContentProviderBulkInsert)

## Code Quality

* Manual check
* Reformat code (Ctrl+Alt+L)
* Optimize imports
* Inspect code
* Code cleanup

## Services

Background tassk

"More background" than Loader (more front-end)
Loaders outlasts configuration changes
Services outlasts activites

Start a service
* Start
  * IntentService
* Schedule
  * JobScheduler
    * FirebaseJobDispatcher
* Bind - for ongoing communication with an activity

Lifecycle:
* A service is started from a context with _startService()_ 
* onCreate()
* onStartCommadn()
* Service is running
* Create AsyncTask
* stopSelf()
* onDestroy()

### IntentService

Automatically runs on the background thread in order, perfect for one off tasks that need to be handled in the background.

[Comparing T10.01-Exercise-IntentServices...T10.01-Solution-IntentServices · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/compare/T10.01-Exercise-IntentServices...T10.01-Solution-IntentServices)


### JobService

Runs on the main thread.

[Adding a JobService - YouTube](https://www.youtube.com/watch?v=vZBxSDhXDlc)
[Exercise: Schedule with FirebaseJobDispatcher - YouTube](https://www.youtube.com/watch?v=lVwknCi7i_s)

It’s important that we verify that we’ve imported `jobdispatcher.JobService` rather than the Android framework’s `JobService`, because if you do, you’ll definitely have some headaches. Double and triple check that please.

### ForegroundService

Service required to have a non-dismissible ongoing notification. Less likely to be destroyed when memory gets low.

## JobScheduler

### FirebaseJobDispatcher

* Add Gradle dependeency
* Create a task to be runned
* Create a service extending JobService
* Add the JobService to the Manifest
* Schedule the JobService with FirebaseJobDispatcher

Example
```
Driver driver = new GooglePlayDriver(context);
FirebaseJobDispatcher dispatcher = new FirebaseJobDispatcher(driver);

Job myJob = dispatcher.newJobBuilder()
    // the JobService that will be called
    .setService(MyJobService.class)
    // uniquely identifies the job
    .setTag("complex-job")
    // one-off job
    .setRecurring(false)
    // don't persist past a device reboot
    .setLifetime(Lifetime.UNTIL_NEXT_BOOT)
    // start between 0 and 15 minutes (900 seconds)     
    .setTrigger(Trigger.executionWindow(0, 900))
    // overwrite an existing job with the same tag
    .setReplaceCurrent(true)
    // retry with exponential backoff 
    .setRetryStrategy(RetryStrategy.DEFAULT_EXPONENTIAL)
    // constraints that need to be satisfied for the job to run
    .setConstraints(
        // only run on an unmetered network
        Constraint.ON_UNMETERED_NETWORK,
        // only run when the device is charging
        Constraint.DEVICE_CHARGING
    )
    .build();
```

[Scheduling Jobs - YouTube](https://www.youtube.com/watch?v=bTFIr9pWnCg)
[The Firebase JobDispatcher](https://github.com/firebase/firebase-jobdispatcher-android)

[Comparing T10.04-Exercise-PeriodicSyncWithJobDispatcher...T10.04-Solution-PeriodicSyncWithJobDispatcher · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/compare/T10.04-Exercise-PeriodicSyncWithJobDispatcher...T10.04-Solution-PeriodicSyncWithJobDispatcher)

## String resources

### Pluralization

XML
```
<plurals name="charge_notification_count">
   <item quantity="zero">Hydrate while charging reminder sent %d times</item>
   <item quantity="one">Hydrate while charging reminder sent %d time</item>
   <item quantity="other">Hydrate while charging reminder sent %d times</item>
</plurals>
```

Java
```
String formattedChargingReminders = getResources().getQuantityString(R.plurals.charge_notification_count, chargingReminders, chargingReminders);
```

[Documentation](https://developer.android.com/guide/topics/resources/string-resource.html#Plurals)


## PendingIntent

Intent in your app designed to be started by another app/service.

This allows a notification (which is handled by the NotificationManager (a system service)) to start your App.

## Notifications

* Use NotificationCompat.Builder to create notifications.
* Get the NotificationManager: `context.getSystemService(Context.NOTIFICATION_SERVICE)`
* Notify! `notificationManager.notify(...)`

Use a PendingIntent to open your App from a notification.

[Notifications - Patterns - Material design guidelines](https://material.io/guidelines/patterns/notifications.html#)

[Notifications | Android Developers](https://developer.android.com/guide/topics/ui/notifiers/notifications.html)
[Using Big View Styles | Android Developers](https://developer.android.com/training/notify-user/expanded.html)
[Notification.BigPictureStyle | Android Developers](https://developer.android.com/reference/android/app/Notification.BigPictureStyle.html)

[Comparing T10.02-Exercise-CreateNotification...T10.02-Solution-CreateNotification · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/compare/T10.02-Exercise-CreateNotification...T10.02-Solution-CreateNotification)

[Add actions to notifications](https://github.com/udacity/ud851-Exercises/compare/T10.03-Exercise-NotificationActions...T10.03-Solution-NotificationActions)

## Memory prioritization

* Critical
	* Active apps
    * Foreground processes
* High
	* Visible processes
* Medium
    * Service processes
* Low
   * Background processes
   * Empty processes
   
## Broadcast Receiver

System Broadcast Intents - triggers for various device changes. 

Creating a broadcast receiever: 

* Static - triggered even when app is offline
* Dynamic - dependent on apps lifecycle

To handle broadcasts when app isn't started: JobDispatcher or in some cases a static broadcast receiver
To handle broadcasts when app is started: dynamic broadcast receiver

Register in onResume() and unregister in onPause if it only is needed for foreground stuff.

[Comparing T10.05-Exercise-ChargingBroadcastReceiver...T10.05-Solution-ChargingBroadcastReceiver · udacity/ud851-Exercises](https://github.com/udacity/ud851-Exercises/compare/T10.05-Exercise-ChargingBroadcastReceiver...T10.05-Solution-ChargingBroadcastReceiver)

## Android Debug Bridge


Start app
```
adb shell am start -n com.package.name/com.package.name.ActivityName
```

Simulate unplugging from USB
```
adb shell dumpsys battery set usb 0
```

Above for Android 6.0+
```
adb shell dumpsys battery unplug
```

Simulate plugging into power 
```
adb shell dumpsys battery reset
```

[Android Debug Bridge | Android Studio](https://developer.android.com/studio/command-line/adb.html?utm_source=udacity&utm_medium=mooc&utm_term=android&utm_content=adb&utm_campaign=training)

## View and View Groups

Avoid nesting view and viewgroups too deep.

General rule of thumb:
* Avoid more than 80 views 
* Avoid more than 10 nested groups

[Views & View Groups - YouTube](https://www.youtube.com/watch?v=8agCiQzDZys)

[Correct the ImageView's adjustViewBounds behaviour on API Level 17 and below with AdjustableImageView :: The Cheese Factory](https://inthecheesefactory.com/blog/correct-imageview-adjustviewbounds-with-adjustable-imageview/en)

### ViewGroups

#### FrameLayout

#### LinearLayout

#### RelativeLayout

#### GridLayout

#### ConstraintLayout

Center vertically by putting a top-constraint to the bottom of the other view, and a bottom-constraint to the top of the other view 

## TextAppearance

Captions

	@style/TextAppearance.AppCompat.Captiom
    
Headline

	@style/TextAppearance.AppCompat.Display1
    
## Hierarchy viewer

Tools > Device monitor > Perspective > Hierarcy viewer

## Accessibility

* TalkBack - screen reader
* Explore by Touch - makes TalkBack speak whatever is being touched
* Accessibility settings - display and sound options

- Use `contentDescription` on all ImageViews, ImageButtons and Checkboxes
	- Text labels, buttons with text and EditTexts normally do not need contentDescription
    - Don't forget contentDescription on dynamically added views
- Enable focus-based navigation
- No audio-only feedback

[Accessibility Developer Checklist | Android Developers](https://developer.android.com/guide/topics/ui/accessibility/checklist.html#recommendations)

## Localization

[Localization Checklist | Android Developers](https://developer.android.com/distribute/tools/localization-checklist.html)
[ISO 639-2 Language Code List - Codes for the representation of names of languages (Library of Congress)](https://www.loc.gov/standards/iso639-2/php/code_list.php)
    
    
## RecyclerView

Different views in a RecyclerView
[Comparing S11.02-Exercise-TodayListItem...S11.02-Solution-TodayListItem · udacity/ud851-Sunshine](https://github.com/udacity/ud851-Sunshine/compare/S11.02-Exercise-TodayListItem...S11.02-Solution-TodayListItem)

* [android - RecyclerView store / restore state between activities - Stack Overflow](http://stackoverflow.com/questions/28236390/recyclerview-store-restore-state-between-activities/28262885#28262885)

## DesignSupportLibrary

* [CoordinatorLayout](http://antonioleiva.com/collapsing-toolbar-layout/)
