---
title: 'getPlayerArmor'
---
# `function` getPlayerArmor <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the equipped armor instance name for a player or NPC.

## Declaration
```cpp
string|nil getPlayerArmor(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `string|nil`
Equipped armor instance, or nil if no armor is equipped.
