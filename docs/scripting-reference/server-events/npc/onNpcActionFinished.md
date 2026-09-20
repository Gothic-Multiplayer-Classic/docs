---
title: 'onNpcActionFinished'
---
# `event` onNpcActionFinished <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when an action leaves the queue through completion, failure, cancellation or timeout.

## Parameters
```c++
void onNpcActionFinished(number npc_id, number action_type, number action_id, boolean result)
```

* `number` **npc_id**: NPC id.
* `number` **action_type**: ACTION_PLAY_ANI.
* `number` **action_id**: Finished action id.
* `boolean` **result**: True only for successful completion reported by the current host.
