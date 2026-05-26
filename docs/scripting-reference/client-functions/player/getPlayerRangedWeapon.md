---
title: 'getPlayerRangedWeapon'
---
# `function` getPlayerRangedWeapon <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the equipped ranged weapon instance name for a player or NPC.

## Declaration
```cpp
string|nil getPlayerRangedWeapon(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `string|nil`
Equipped ranged weapon instance, or nil if none is equipped.
