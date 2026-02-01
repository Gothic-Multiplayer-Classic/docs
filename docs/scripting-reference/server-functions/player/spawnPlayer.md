---
title: 'spawnPlayer'
---
# `function` spawnPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    If the player is not spawned, server doesn't recognize his presence at all.

Spawn a player, optionally overriding the spawn position.

## Declaration
```cpp
boolean spawnPlayer(int player_id, {x, y, z} Optional)
```

## Parameters
* `int` **player_id**: Player id to spawn.
* `{x, y, z}` **Optional**: position table or three numeric coords.
  
## Returns `boolean`
True on success, false if the player is missing.
