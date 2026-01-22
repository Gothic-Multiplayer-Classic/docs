---
title: 'setPlayerRespawnTime'
---
# `function` setPlayerRespawnTime <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    The respawnTime can't be smaller than 1001 miliseconds.

This function will set the player time to respawn after death. If set to 0, respawn is disabled for selected player.

## Declaration
```cpp
void setPlayerRespawnTime(int player_id, int respawn_time)
```

## Parameters
* `int` **player_id**: Target player id.
* `int` **respawn_time**: New respawn time in milliseconds.
