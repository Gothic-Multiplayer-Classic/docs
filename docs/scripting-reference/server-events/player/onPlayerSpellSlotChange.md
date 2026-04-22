---
title: 'onPlayerSpellSlotChange'
---
# `event` onPlayerSpellSlotChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's active spell slot changes.

## Parameters
```c++
void onPlayerSpellSlotChange(number player_id, number slot_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number` **slot_id**: Active spell slot id.
* `number|nil` **instance**: Spell instance id (nil if none).
