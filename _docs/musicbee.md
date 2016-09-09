---
title: MusicBee
tags:
  - apps
published: true
---

# MusicBee

## Views

### Default Album and Tracks view

#### Preferences > Layout(1) > Customize Layout > Configure Fields

Original label | Override label   | Alignment
---------------|------------------|----------
#              | `Playlist Track` | Right
Artwork        | `Artwork`        | Middle
Love           | `♥`              | Middle
Track#         | ` # `            | Right

#### Displayed fields 

- Artwork
- ♥
- #
- _Title short_
- Rating 
- _Featuring_


 Artwork | ♥ | # | _Title short_ | Rating | Time |  _Featuring_
|:------:|:-:|--:|:--------------|:-------|-----:|:-----------|
    ☺    | ♥ | 1 | The End       | ☼☼☼☼☼  | 3:58 | 


## Virtual tags

Label | Formula 
------|------------------------------------
Title Short     | `$Split(<Title>," (feat",1)` 




