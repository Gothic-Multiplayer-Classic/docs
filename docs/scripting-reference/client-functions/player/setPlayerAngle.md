---
title: 'setPlayerAngle'
---
# `function` setPlayerAngle <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC facing angle in world space.

## Declaration
```cpp
boolean setPlayerAngle(number player_id, number angle)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **angle**: Angle in degrees.
  
## Returns `boolean`
True on success.
