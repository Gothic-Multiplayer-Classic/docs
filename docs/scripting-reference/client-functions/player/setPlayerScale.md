---
title: 'setPlayerScale'
---
# `function` setPlayerScale <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC model scale.

## Declaration
```cpp
boolean setPlayerScale(number player_id, number x, number y, number z)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **x**: Scale factor on x axis.
* `number` **y**: Scale factor on y axis.
* `number` **z**: Scale factor on z axis.
  
## Returns `boolean`
True on success.
