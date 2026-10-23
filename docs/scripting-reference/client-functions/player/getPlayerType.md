---
title: 'getPlayerType'
---
# `function` getPlayerType <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    Accepts player and server NPC ids; negative client-local NPC ids are not supported.

This function will return the multiplayer player type.

## Declaration
```cpp
number|nil getPlayerType(number player_id)
```

## Parameters
* `number` **player_id**: Target player or server NPC id; client-local NPC ids are not supported.
  
## Returns `number|nil`
Player type, or nil if unavailable.
