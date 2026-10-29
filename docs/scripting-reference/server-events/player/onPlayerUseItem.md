---
title: 'onPlayerUseItem'
---
# `event` onPlayerUseItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event can be cancelled.

This event is triggered when the player/npc attempts to use an item.

## Parameters
```c++
void onPlayerUseItem(number player_id, string|nil item, number quantity, string scheme)
```

* `number` **player_id**: Player/npc using the item.
* `string|nil` **item**: Item instance name, or nil for an empty slot.
* `number` **quantity**: Amount consumed; zero for a reusable item.
* `string` **scheme**: Native use scheme reported by the controlling client.
