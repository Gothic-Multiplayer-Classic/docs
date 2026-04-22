---
title: 'getPlayerTalent'
---
# `function` getPlayerTalent <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/npc talent value, or nil if unavailable.

## Declaration
```cpp
number|nil getPlayerTalent(number player_id, number talent_id)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **talent_id**: Talent identifier.
  
## Returns `number|nil`
Talent value or nil.
