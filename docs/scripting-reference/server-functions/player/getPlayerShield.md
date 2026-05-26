---
title: 'getPlayerShield'
---
# `function` getPlayerShield <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player's equipped shield instance name.

## Declaration
```cpp
string|nil getPlayerShield(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `string|nil`
Equipped shield instance, or nil if no shield is equipped.
