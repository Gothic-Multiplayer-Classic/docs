---
title: 'setPlayerRespawnTime'
---
# `function` setPlayerRespawnTime <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will set a player's automatic respawn delay in milliseconds. Zero disables automatic respawn for that player.

## Declaration
```cpp
boolean setPlayerRespawnTime(number player_id, number respawn_time)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **respawn_time**: New respawn time in milliseconds.
  
## Returns `boolean`
True on success; false for an unknown player or a negative duration.
