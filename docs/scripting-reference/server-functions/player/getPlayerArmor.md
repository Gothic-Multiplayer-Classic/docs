---
title: 'getPlayerArmor'
---
# `function` getPlayerArmor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player's equipped armor instance name.

## Declaration
```cpp
string|nil getPlayerArmor(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `string|nil`
Equipped armor instance, or nil if no armor is equipped.
