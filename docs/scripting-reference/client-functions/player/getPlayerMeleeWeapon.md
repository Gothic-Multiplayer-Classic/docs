---
title: 'getPlayerMeleeWeapon'
---
# `function` getPlayerMeleeWeapon <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the equipped melee weapon instance name for a player or NPC.

## Declaration
```cpp
string|nil getPlayerMeleeWeapon(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `string|nil`
Equipped melee weapon instance, or nil if none is equipped.
