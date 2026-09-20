---
title: 'getNpcAnimation'
---
# `function` getNpcAnimation <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns the stored persistent animation, independently of the finite queue.

## Declaration
```cpp
string|nil getNpcAnimation(number npc_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
  
## Returns `string|nil`
Animation name, empty when cleared; nil for a missing NPC.
