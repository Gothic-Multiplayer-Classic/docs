---
title: 'getNpcHostPlayer'
---
# `function` getNpcHostPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns the player currently responsible for executing this NPC's actions.

## Declaration
```cpp
number getNpcHostPlayer(number npc_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
  
## Returns `number`
Player id, or -1 when unhosted or missing.
