---
title: 'getPlayerRespawnTime'
---
# `function` getPlayerRespawnTime <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Get the player time to respawn after death.

## Declaration
```cpp
number|nil getPlayerRespawnTime(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `number|nil`
The player respawn time or nil if player isn't created.
