---
tags:
  - windows
title: Windows 10 Essentials
published: true
---

Windows 10 Essentials
=====================

* TOC
{:toc}

## Before formatting

### Backup
* Speed Dial settings
* StackEdit docs and settings
* Android Studio settings
* List of extensions for Atom and Brackets
* PuTTY sessions
	`regedit /e "D:\postmorten_win10\Backup\PuTTY\putty-sessions.reg" HKEY_CURRENT_USER\Software\Simontatham`

### Download
* AMD Drivers
  * _Desktop Graphics Radeon HD 5700 Series PCIe Windows 10 - 64 bit_

## During installation
Skip serial -- activation is done automatically


Drivers
-------

### Graphic drivers
* Install
* Disable "Gaming Evolved App"
* AMD Catalyst Control Center > Preferences > Disable System Tray Menu

### Motherboard
1_mb_driver_chipset_intel
2_motherboard_driver_intel_sataraid_irst
3_motherboard_driver_sata_gb_sata2raid_5series
4_motherboard_driver_marvell_console
5_motherboard_driver_usb3

### Asus PCE-AC68 Driver and Utilities
 * Use english
 * Install driver only using .iso and Device Manager
 * Enable beamforming

### akasa Smart Card Reader
> **Drivers:** http://www.akasa.com.tw/search.php?seed=AK-ICR-05


Tweaks
------

### Connect to DS713+
* In Explorer, open `\\DS713`
* Enter user and password
* For folder "samba", map network drive: `Z:`
* Rename `Z:` to `DS713+`
* Customize Quick access and Windows Start Menu

### Switch to a local account

### Map personal folders
`C:\Users\Oscar\<FOLDER>  -> D:\Users\Oscar\<FOLDER>`
where `<FOLDER>` is 
 * Desktop
 * Documents
 * Downloads
 * Music
 * Pictures
 * Videos

### Treat as internal
* Run treatasinternal.reg

### Change user profile picture

### Disable password
`Win+R` `control userpasswords2`

### Explorer
 * Show extensions for known file types
 * Show hidden files
 * Open file explorer to _This PC_

### Windows Control Panel
 * Control Panel > User Accounts > Manage User Account Control settings > Never notify
 * Control Panel > Language > Advanced settings > Change language bar hot keys
 * Control Panel > Mouse: Mouse speed
 * Control Panel > Power Options 
 * Control Panel > Windows Update
   * Select "Notify to schedule restart"
   * Run update
   
### Windows Settings 
 * Settings > System > Multitasking > Disable Snap Assist
 
### Windows Start Menu

> **Put monitors to sleep**
> C:\Users\Oscar\AppData\Roaming\Microsoft\Windows\Start Menu\Programs

### Windows Taskbar
Create the following web apps using Chrome and pin to taskbar

 * Tasks
   `https://mail.google.com/tasks/ig`
 * Keep
 * Prose.io
 * Spotify
 * MusicBee
 * WorkFlowy
 * Video Station
 
Refresh icon cache with `ie4uinit.exe -show` 
 
> **Location:** C:\Users\Oscar\AppData\Roaming\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar

### Mouse and keyboard
**Mouse**
Edit wheel speed, middle click, left side button and right side button

### Screen-saver
Enable screen-saver for 9 minutes

### Remove OneDrive

How to Get Rid of the OneDrive Icon in Windows 10's File Explorer
http://lifehacker.com/how-to-get-rid-of-the-onedrive-icon-in-windows-10s-file-1722592615

Software
--------

### Adobe Photoshop

### Adobe Illustrator



### SDFormatter

### Realtek HD Audio manager
Remove notification icon

### OneDrive
Disable "Start OneDrive on startup" from OneDrive settings


### WinRAR
Settings > Compression > Remove redundant folders from extraction path
> C:\Users\Oscar\AppData\Roaming\WinRAR

### PuTTY
 * Login to DS713
 * Save session
 * Settings > Window > Behaviour > Full-screen on Alt+Enter 
 * Edit Windows Start shortcut to start saved session directly
	 * Append ` -load "DS713+"`
 * Pin to Start.

> **Running as a portable app**
> D:\apps\PuTTY
> 
> **Download**
> http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html

### Dropbox
  * Preferences > Share screenshots using Dropbox
  * Don't limit upload rate 

### VLC

### Spotify
* Connect to Last.fm

### Chrome

#### Extensions

* Adblock Plus
* cookies.txt
* Keep Chrome Extension
* LastPss
* Markdown here
* Postman
* prose
* RSS
* Save to Pocket
* Speed Dial 2
* Stop YouTube Autoplay
* Stylish
* TabCopy
* Tampermonkey


#### LastPass
 * Preferences > Advanced > Show Matching Sites in top level menu

> **NOTE**
> Set to english

** Silence with one click **
 * Go to `chrome://flags`
 * Enable _Enable tab audio_

* Import SpeedTab settings


#### Stylish

**WorkFlowy Yellow Star**
```
.pageStar.starred {
    background-image: url(/media/i/star-icon-empty.svg);
    background-color: yellow;
    -webkit-mask-image: url(/media/i/star-icon-grey.svg);
    -webkit-mask-size: 20px;
}
```


### Transmission Remote GUI

> **Website:** https://code.google.com/p/transmisson-remote-gui/
> **Paths:** /volume1/downloads=Z:\downloads



### Development

### Android Studio


### Atom
#### Settings
Settings > Scroll past end

#### Packages

Generate with `apm list --installed --bare`

* auto-detect-indentation@1.0.0
* autoclose-html@0.23.0
* compare-files@0.6.2
* expose@0.11.1
* git-plus@5.13.0
* git-time-machine@1.3.0
* highlight-selected@0.11.2
* keyboard-localization@1.4.10
* merge-conflicts@1.3.7
* minimap@4.21.0
* open-recent@5.0.0
* remote-edit@1.8.22
* Remote-FTP@0.7.10
* rest-client@1.0.0
* split-diff@0.5.3


#### Brackets

Extensions
* [zaggino/brackets-git: brackets-git](https://github.com/zaggino/brackets-git) 

#### Node.js

#### FileZilla

#### Git

#### Java

### Try 2016-08

* [John’s Background Switcher | John's Adventures](https://johnsad.ventures/software/backgroundswitcher/)

* [Top 10 Places to Get Stunning Desktop Wallpaper](http://lifehacker.com/top-10-places-to-get-stunning-desktop-wallpaper-1781991380)

#### Rainmeter

https://www.rainmeter.net/

* [MinimalOne Weather 1.0 by mistrjosh on DeviantArt](http://mistrjosh.deviantart.com/art/MinimalOne-Weather-1-0-510234680)
* [Simple Clean by HipHopium on DeviantArt](http://hiphopium.deviantart.com/art/Simple-Clean-593429217)
* [TextClock 2.1 by jsmorley on DeviantArt](http://jsmorley.deviantart.com/art/TextClock-2-1-609165064)

#### Launchy

* [Launchy: The Open Source Keystroke Launcher](http://www.launchy.net/)
  * [Why You Should Be Using an App Launcher (and How to Make It Do More Than Launch Apps)](http://lifehacker.com/5963597/why-you-should-be-using-an-app-launcher-and-how-to-make-it-do-anything-you-want#_ga=1.98741918.1667622160.1441735094)
  * [How to Create a Shortcut for Any "Modern" Windows App](http://lifehacker.com/how-to-create-a-shortcut-for-any-modern-windows-app-1722569853)
* LibreOffice
	* [Home LibreOffice - Free Office Suite - Fun Project - Fantastic People](https://www.libreoffice.org/)
* [Download Sumatra PDF - a free reader](http://www.sumatrapdfreader.org/download-free-pdf-viewer.html)
* [Online Data Backup  Offsite, Onsite & Cloud Crashplan](https://www.crashplan.com/en-us/)
* [f.lux: software to make your life better](https://justgetflux.com/)
* [Avira 2016 - Download free antivirus for PC & Mac](http://www.avira.com/)
* [Bins™, by 1UP Industries](http://www.1upindustries.com/bins/)


http://winaero.com/blog/move-notification-toasts-to-top-or-bottom-of-the-screen-in-windows-10/
