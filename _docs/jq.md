---
tags:
  - apps
published: true
---


# jq

## Recipies 


Combine multiple json files with arrays into one json file
```
jq -s '[.[][]]' *.json > all.json
```
