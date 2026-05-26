---
title: 'getPlayerShield'
---
# `function` getPlayerShield <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the equipped shield instance name for a player or NPC.

## Declaration
```cpp
string|nil getPlayerShield(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `string|nil`
Equipped shield instance, or nil if no shield is equipped.
