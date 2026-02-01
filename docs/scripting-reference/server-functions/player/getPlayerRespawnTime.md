---
title: 'getPlayerRespawnTime'
---
# `function` getPlayerRespawnTime <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Get the player time to respawn after death.

## Declaration
```cpp
int|nil getPlayerRespawnTime(int player_id)
```

## Parameters
* `int` **player_id**: Target player id.
  
## Returns `int|nil`
The player respawn time or nil if player isn't created.
