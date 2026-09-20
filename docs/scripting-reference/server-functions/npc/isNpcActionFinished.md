---
title: 'isNpcActionFinished'
---
# `function` isNpcActionFinished <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Checks whether an allocated action has left the queue, including failure or cancellation.
A true result does not imply success. Use onNpcActionFinished's result argument
to distinguish successful completion from failure, timeout or cancellation.

## Declaration
```cpp
boolean isNpcActionFinished(number npc_id, number action_id)
```

## Parameters
* `number` **npc_id**: Server NPC id.
* `number` **action_id**: Action id returned by npcPlayAnimation.
  
## Returns `boolean`
True once the action is no longer queued; false for unknown ids.
