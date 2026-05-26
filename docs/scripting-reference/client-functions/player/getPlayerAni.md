---
title: 'getPlayerAni'
---
# `function` getPlayerAni <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the active animation name for a player or NPC.

## Declaration
```cpp
string|nil getPlayerAni(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `string|nil`
Active animation name, or nil if unavailable.
