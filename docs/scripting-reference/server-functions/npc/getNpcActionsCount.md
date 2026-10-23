---
title: 'getNpcActionsCount'
---
# `function` getNpcActionsCount <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns the number of running and pending actions.

## Declaration
```cpp
number|nil getNpcActionsCount(number npc_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
  
## Returns `number|nil`
Queue size, or nil for a missing NPC.
