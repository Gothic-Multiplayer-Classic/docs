---
title: 'spawnPlayer'
---
# `function` spawnPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    If the player is not spawned, server doesn't recognize his presence at all.

This function will spawn the player, optionally overriding the spawn position.

## Declaration
```cpp
boolean spawnPlayer(number player_id, {x, y, z}|nil position)
```

## Parameters
* `number` **player_id**: Player id to spawn.
* `{x, y, z}|nil` **position**: Optional position table or three numeric coords.
  
## Returns `boolean`
True on success.
