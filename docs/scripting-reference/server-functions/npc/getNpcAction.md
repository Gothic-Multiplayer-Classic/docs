---
title: 'getNpcAction'
---
# `function` getNpcAction <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns a copy of an action's metadata. Index zero is the queue head.

## Declaration
```cpp
{id, type, status, animation, timeout_ms}|nil getNpcAction(number npc_id, number index)
```

## Parameters
* `number` **npc_id**: Server NPC id.
* `number` **index**: Zero-based queue index.
  
## Returns `{id, type, status, animation, timeout_ms}|nil`
Action snapshot, or nil for an invalid NPC or index.
