---
title: 'getPlayerHelmet'
---
# `function` getPlayerHelmet <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the equipped helmet instance name for a player or NPC.

## Declaration
```cpp
string|nil getPlayerHelmet(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `string|nil`
Equipped helmet instance, or nil if no helmet is equipped.
