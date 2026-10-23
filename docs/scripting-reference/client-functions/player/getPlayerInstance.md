---
title: 'getPlayerInstance'
---
# `function` getPlayerInstance <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC current instance, or nil if unavailable.

## Declaration
```cpp
string|nil getPlayerInstance(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `string|nil`
Instance name or nil.
