---
title: MusicBee
tags:
  - apps
published: true
---

# MusicBee

## Views

### Default Album and Tracks view


#### Preferences > Layout(1) > Main Panel > Customize Layout

Grouping header | Font | Contrast
----------------|------|----------
L: `Album Artist` | Roboto Light, 16pt | 90%
R:              |      | 






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
9   | Album Year    | Save to MusicBee database only
10  | Edition       | Save to MusicBee database only

### Identifiers

* Game
* Game Series
* Song
* Platform
* Album Year

## Virtual tags

Song
: ``` 
  $Split(<Title>," (feat",1)
  ``` 
  
Disc Nr
: ```
  $If($Group(<Disc#>,3)="0-9",$If(<Disc Count>>1,"Disc "<Disc#>$IsNull(<Edition>,," - "),),"Vol. "<Disc#>": "<Grouping>)$IsNull(<Edition>,,<Edition>)
  ``` 


