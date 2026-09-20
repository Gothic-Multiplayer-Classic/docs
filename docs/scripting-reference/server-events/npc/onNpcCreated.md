---
title: 'onNpcCreated'
---
# `event` onNpcCreated <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Reports NPC creation at the end of the server tick. The NPC may already be spawned or destroyed.

## Parameters
```c++
void onNpcCreated(number npc_id)
```

* `number` **npc_id**: Created NPC id.
