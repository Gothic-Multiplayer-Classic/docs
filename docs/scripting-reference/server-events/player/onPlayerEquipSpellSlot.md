---
title: 'onPlayerEquipSpellSlot'
---
# `event` onPlayerEquipSpellSlot <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event can be cancelled.

This event is triggered when a player's active spell slot changes.

## Parameters
```c++
void onPlayerEquipSpellSlot(number player_id, number slot_id, Item|nil item, Item|nil previous_item)
```

* `number` **player_id**: Player id.
* `number` **slot_id**: Active spell slot id (0 if none).
* `Item|nil` **item**: Active spell item (nil if none).
* `Item|nil` **previous_item**: Previously equipped item.
