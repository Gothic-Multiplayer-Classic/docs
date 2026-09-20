---
title: 'getNpcLastActionId'
---
# `function` getNpcLastActionId <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns the most recently allocated action id, including completed actions.

## Declaration
```cpp
number getNpcLastActionId(number npc_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
  
## Returns `number`
Action id, zero before any actions, or -1 for a missing NPC.
