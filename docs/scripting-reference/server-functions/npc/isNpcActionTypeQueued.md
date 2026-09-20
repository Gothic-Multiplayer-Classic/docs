---
title: 'isNpcActionTypeQueued'
---
# `function` isNpcActionTypeQueued <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Checks whether the queue contains a running or pending action of the requested type.

## Declaration
```cpp
boolean isNpcActionTypeQueued(number npc_id, number action_type)
```

## Parameters
* `number` **npc_id**: Server NPC id.
* `number` **action_type**: ACTION_PLAY_ANI is the only supported type.
  
## Returns `boolean`
True if the type is present in the queue.
