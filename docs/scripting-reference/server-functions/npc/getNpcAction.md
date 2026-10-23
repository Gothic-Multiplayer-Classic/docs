---
title: 'getNpcAction'
---
# `function` getNpcAction <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns a copy of an action's metadata. Index one is the queue head.

## Declaration
```cpp
{id, type, status, animation, timeoutMs}|nil getNpcAction(number npc_id, number index)
```

## Parameters
* `number` **npc_id**: Server NPC id.
* `number` **index**: One-based queue index.
  
## Returns `{id, type, status, animation, timeoutMs}|nil`
Action snapshot, or nil for an invalid NPC or index.
