---
title: 'getPlayerTalent'
---
# `function` getPlayerTalent <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player's talent value, or nil if unavailable.

## Declaration
```cpp
number|nil getPlayerTalent(number player_id, number talent_id)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **talent_id**: Talent identifier, for more information check [Talent Constants](../../shared-constants/Talent.md).
  
## Returns `number|nil`
Talent value or nil.
