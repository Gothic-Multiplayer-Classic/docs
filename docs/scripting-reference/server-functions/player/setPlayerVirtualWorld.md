---
title: 'setPlayerVirtualWorld'
---
# `function` setPlayerVirtualWorld <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC's virtual world id.

## Declaration
```cpp
boolean setPlayerVirtualWorld(number player_id, number virtual_world)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `number` **virtual_world**: Virtual world id (0-65535).
  
## Returns `boolean`
True on success.
