---
tags: [android]
---

# Tasker


## Profiles

## Tasks




## Secure settings

Enable changing secure settings

```
adb shell pm grant net.dinglisch.android.taskerm android.permission.WRITE_SECURE_SETTINGS
```

See available secure settings
```
adb shell settings list global
adb shell settings list secure
adb shell settings list system
```