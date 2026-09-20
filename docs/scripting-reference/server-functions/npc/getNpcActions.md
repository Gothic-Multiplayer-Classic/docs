---
title: 'getNpcActions'
---
# `function` getNpcActions <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns copies of all running and pending actions in queue order.

## Declaration
```cpp
{...}|nil getNpcActions(number npc_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
  
## Returns `{...}|nil`
One-based Lua array of action snapshots, or nil for a missing NPC.
