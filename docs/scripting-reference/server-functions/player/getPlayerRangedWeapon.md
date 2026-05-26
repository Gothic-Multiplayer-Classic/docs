---
title: 'getPlayerRangedWeapon'
---
# `function` getPlayerRangedWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player's equipped ranged weapon instance name.

## Declaration
```cpp
string|nil getPlayerRangedWeapon(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `string|nil`
Equipped ranged weapon instance, or nil if none is equipped.
