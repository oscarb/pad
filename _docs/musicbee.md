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


## Virtual tags

Label | Formula 
------|---------|---------------------------
Title Short[^1] | `$Split(<Title>," (feat",1)` 


[^1]: Shows titles without featuring artists


### Track titles without featuring artists

Title Short | `$Split(<Title>," (feat",1)` 


### Test

**Title short**
`$Split(<Title>," (feat",1)` 
 
 
### Title short
 `$Split(<Title>," (feat",1)` 





* Title short
	`$Split(<Title>," (feat",1)` 
    

