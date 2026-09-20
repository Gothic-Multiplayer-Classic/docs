---
title: 'onNpcChangeHostPlayer'
---
# `event` onNpcChangeHostPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when the player responsible for executing an NPC's actions changes.

## Parameters
```c++
void onNpcChangeHostPlayer(number npc_id, number current_id, number previous_id)
```

* `number` **npc_id**: NPC id.
* `number` **current_id**: New host id, or -1 for no host.
* `number` **previous_id**: Previous host id, or -1 for no host.
