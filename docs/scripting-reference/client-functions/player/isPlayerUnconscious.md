---
title: 'isPlayerUnconscious'
---
# `function` isPlayerUnconscious <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will check whether a player or NPC is unconscious.

## Declaration
```cpp
boolean|nil isPlayerUnconscious(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `boolean|nil`
Unconscious state, or nil if unavailable.
