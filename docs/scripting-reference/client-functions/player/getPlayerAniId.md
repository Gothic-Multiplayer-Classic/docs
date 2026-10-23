---
title: 'getPlayerAniId'
---
# `function` getPlayerAniId <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the active animation id for a player or NPC.

## Declaration
```cpp
number getPlayerAniId(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `number`
Active animation id, or -1 if unavailable.
