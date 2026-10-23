---
title: 'getPlayerHelmet'
---
# `function` getPlayerHelmet <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC's equipped helmet instance name.

## Declaration
```cpp
string|nil getPlayerHelmet(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `string|nil`
Equipped helmet instance, or nil if no helmet is equipped.
