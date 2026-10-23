---
title: 'getPlayerAngle'
---
# `function` getPlayerAngle <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC's facing angle in degrees, or nil if unavailable.

## Declaration
```cpp
number|nil getPlayerAngle(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `number|nil`
Angle in degrees or nil.
