---
title: MusicBee
tags:
  - apps
published: true
---

# MusicBee

## Filters

* Organized
  * Match `all` of the following rules
  	- Path starts with `D:\Users\archive\Oscar\Music\Library`


## Settings

### General

* Minimize to `Mini Player`



## Views

### Default Album and Tracks view


#### Preferences > Layout(1) > Main Panel > Customize Layout

Grouping header | Font | Contrast
----------------|------|----------
L: `Album Artist` | Roboto Light 16pt | 90%
R:              |      | 


Sub-grouping header | Font | Contrast
--------------------|------|----------
Disc Label          | Roboto Light 12pt | 60%

[ ] Precede with a blank line


Fields displayed: below artwork

Field | Font | Contrast 
------|------|---------------
Album Artist |  |  
Album | Roboto Regular 13pt | 80%
Virtual Album Year | Roboto Regular 10pt | 70%
Album Rating |  | 90%
Custom16 | Roboto Regular 24pt | 30%

[x} Group tracks with a header (Album Artist)  ([ ] except for playlists)
[ ] Display first few tracks only  ([ ] except for playlists)
[x] Do not show artwork for albums with less than `2` tracks







##### Configure Fields

Original label | Override label   | Alignment
---------------|------------------|----------
#              | `Playlist Track` | Right
Artwork        | `Artwork`        | Middle
Love           | `♥`              | Middle
Track#         | ` # `            | Right
Artists: Guest | `Feauturing`     | Left

#### Displayed fields 

 Artwork | ♥ | # | _Title short_ | Rating | Time |  _Featuring_
|:------:|:-:|--:|:--------------|:-------|-----:|:-----------|
    ☺    | ♥ | 1 | The End       | ☼☼☼☼☼  | 3:58 | 


[ ] Keep columns sized to panel 



## Custom tags

### Tags

Tag | Display name  | Save to music file as tag
---:|---------------|------------------------------
1   | Sort Artist   | Artist Sort-Order
2   | Sort Album Artist | Album Artist Sort-Order
3   |  |
4   |  |
5   | Game          | Game
6   | Game Series   | Game Series
7   | Song          | Song
8   | Platform      | Platform 
9   | Album Year    | Album Year
10  | Edition       | Save to MusicBee database only

### Identifiers

* Game
* Game Series
* Song
* Platform
* Album Year

## Virtual tags

Track
: ``` 
  $Split(<Title>," (feat",1)
  ``` 
  
Disc Label v1
: ```
  $If($Group(<Disc#>,3)="0-9",$If(<Disc Count>>1,"Disc "<Disc#>$IsNull(<Edition>,," - "),),"Vol. "<Disc#>": "<Grouping>)$IsNull(<Edition>,,<Edition>)
  ``` 

Disc Label v2
: ```
  $If($Group(<Disc#>,3)="0-9",$If(<Disc Count> > 1,"Disc "<Disc#>$IsNull(<Edition>,," - "<Edition>),),)
  ```
  
Virtual Album Year 
: ```
$IsNull(<Album Year>,$Left(<Year>,4),$Left(<Album Year>,4)
```
