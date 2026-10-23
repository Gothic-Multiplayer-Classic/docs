---
title: 'getNpcHostPlayer'
---
# `function` getNpcHostPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns the player currently responsible for executing this NPC's actions.

## Declaration
```cpp
number|nil getNpcHostPlayer(number npc_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
  
## Returns `number|nil`
Player id, or nil when unhosted or missing.
