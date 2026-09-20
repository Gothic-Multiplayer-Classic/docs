---
title: 'onNpcActionSent'
---
# `event` onNpcActionSent <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when the current action is dispatched to its host. A replay after host migration may emit it again.

## Parameters
```c++
void onNpcActionSent(number npc_id, number action_type, number action_id)
```

* `number` **npc_id**: NPC id.
* `number` **action_type**: ACTION_PLAY_ANI.
* `number` **action_id**: Dispatched action id.
