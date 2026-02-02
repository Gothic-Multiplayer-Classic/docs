---
title: 'setPlayerRespawnTime'
---
# `function` setPlayerRespawnTime <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    The respawnTime can't be smaller than 1001 miliseconds.

Set the player time to respawn after death. If set to 0, respawn is disabled for selected player.

## Declaration
```cpp
void setPlayerRespawnTime(number player_id, number respawn_time)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **respawn_time**: New respawn time in milliseconds.
