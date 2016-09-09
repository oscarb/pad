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
L: Album Artist | Roboto Light, 16pt | 90%
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


## Virtual tags

Label | Formula 
------|------------------------------------
Song  | `$Split(<Title>," (feat",1)` 
Disc Nr | ```$If($Group(<Disc#>,3)="0-9",$If(<Disc Count>>1,"Disc "<Disc#>$IsNull(<Edition>,," - "),),"Vol. "<Disc#>": "<Grouping>)$IsNull(<Edition>,,<Edition>)``` 


Song
:  `$Split(<Title>," (feat",1)` 

Disc Nr
: ```$If($Group(<Disc#>,3)="0-9",$If(<Disc Count>>1,"Disc "<Disc#>$IsNull(<Edition>,," - "),),"Vol. "<Disc#>": "<Grouping>)$IsNull(<Edition>,,<Edition>)``` 


