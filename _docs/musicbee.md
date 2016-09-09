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
Artists: Guest | `Feauturing`     | Left

#### Displayed fields 

 Artwork | ♥ | # | _Title short_ | Rating | Time |  _Featuring_
|:------:|:-:|--:|:--------------|:-------|-----:|:-----------|
    ☺    | ♥ | 1 | The End       | ☼☼☼☼☼  | 3:58 | 

- [ ] Keep columns sized to panel 

## Virtual tags

Label | Formula 
------|------------------------------------
Song  | `$Split(<Title>," (feat",1)` 




