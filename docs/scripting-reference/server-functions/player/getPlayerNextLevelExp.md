---
title: 'getPlayerNextLevelExp'
---
# `function` getPlayerNextLevelExp <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the experience required for the player/NPC's next level, or nil if unavailable.

## Declaration
```cpp
number|nil getPlayerNextLevelExp(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `number|nil`
Next level exp or nil.
