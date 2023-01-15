---
title: macOS Essentials
tags:
  - macOS
published: true
---

# macOS Essentials

## Backup 

- Files
- App settings
- System settings
- Notes
- Postman
- Bookmarks
- Pictures/movies taken with webcam

### Android Studio 

Scratches

## Set Up

- Apps
- System settings
- Tweaks


### Apps

- Homebrew
- Android Studio 
- Figma
- Focusrite Control
- Chrome
- GraphQL Playground
- Kap
- scrcpy
- Keybase
- LastPass
- Logi Options
- Microsoft Teams
- Postman
- Scroll Reverser?
- Slack
- [Rectangle](https://github.com/rxhanson/Rectangle)
- Spotify
- SpotMenu
- Transmission Remote GUI
- Visual Studio Code
- Visual Studio Code - Insiders
- VLC
- WhatsApp

#### Homebrew

Install Homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Install tools
```
brew install scrcpy
```

Install apps
```
brew cask install figma google-chrome kap lastpass microsoft-teams slack rectangle spotify spotmenu transmission-remote-gui visual-studio-code vlc
```

* https://brew.sh/


#### Android Studio 

Add ADB to Path

```
export ANDROID_HOME=/Users/$USER/Library/Android/sdk
export ANDROID_SDK_ROOT=$ANDROID_HOME
PATH="$PATH:$ANDROID_HOME/emulator:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools"
```
#### Chrome

* Set upp web apps for DSM
* Update chrome://flags/#unsafely-treat-insecure-origin-as-secure 


### System settings

- Log in with Exchange account
- Turn on [Do not disturb when screen is sleeping/locked](https://www.jeffgeerling.com/blog/2016/external-display-waking-disable-notifications-when-your-screen)


### Tweaks

- SSH
- Change resolution of built-in retina screen
- Automatically hide/show dock
- Hide desktop icons
- Disable Keyboard shortcut "Search man Page Index in Terminal" (interfers with Android Studio)

#### SSH

Generate SSH keys: 
https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key


## Development

* [Change PATH](https://stackoverflow.com/questions/14637979/how-to-permanently-set-path-on-linux-unix/14638025#14638025)

### Python 3

```
 brew install python
```

See [Installing Python 3 on Mac OS X](https://docs.python-guide.org/starting/install3/osx/)


## Settings

### General 

* Sidebar icon size: small
* Default web browser: Chrome

### Dock

* Show and hide automatically

### Shortcuts

* Mission Control

Move left a space: cmd + >
Move right a space: cmd + <


## Issues

### Low Bluetooth Audio Quailty

Enter in terminal

    sudo killall coreaudiod
    
Or change sound input away from bluetooth, see http://superuser.com/a/1163164

## Tips

https://www.reddit.com/r/macbookpro/comments/106ryt9/comment/j3k1yw4/?utm_source=share&utm_medium=web2x&context=3
