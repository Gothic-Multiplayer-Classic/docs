---
title: 'setPlayerPosition'
---
# `function` setPlayerPosition <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/npc position.

## Declaration
```cpp
boolean setPlayerPosition(number player_id, number x, number y, number z, boolean|nil interpolate)
```

## Parameters
* `number` **player_id**: Target player or server NPC id.
* `number` **x**: X coordinate.
* `number` **y**: Y coordinate.
* `number` **z**: Z coordinate.
* `boolean|nil` **interpolate**: Whether to interpolate movement. Defaults to false for players and true for NPCs.
  
## Returns `boolean`
True on success.
