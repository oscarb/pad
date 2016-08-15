---
tags: [windows]
title: Windows 10 Essentials
---

Windows 10 Essentials
=====================

* TOC
{:toc}

## Before formatting

### Backup
* SpeedTab settings
* StackEdit docs and settings

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
 * StackEdit
 * Spotify
 * MusicBee
 
> **Location:** C:\Users\Oscar\AppData\Roaming\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar

### Mouse and keyboard
**Mouse**
Edit wheel speed, middle click, left side button and right side button

### Screen-saver
Enable screen-saver for 9 minutes


Software
--------

### SDFormatter

### Realtek HD Audio manager
Remove notification icon

### OneDrive
Disable "Start OneDrive on startup" from OneDrive settings

### Atom
Settings > Scroll past end

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

### Chrome

#### LastPass
 * Preferences > Advanced > Show Matching Sites in top level menu

> **NOTE**
> Set to english

** Silence with one click **
 * Go to `chrome://flags`
 * Enable _Enable tab audio_

* Import SpeedTab settings


### Transmission Remote GUI

> **Website:** https://code.google.com/p/transmisson-remote-gui/
> **Paths:** /volume1/downloads=Z:\downloads




http://winaero.com/blog/move-notification-toasts-to-top-or-bottom-of-the-screen-in-windows-10/