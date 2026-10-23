---
title: 'onPlayerHit'
---
# `event` onPlayerHit <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player is hit.

## Parameters
```c++
void onPlayerHit(number|nil attacker_id, number victim_id, number damage, number damageType)
```

* `number|nil` **attacker_id**: Optional attacker id (nil if none).
* `number` **victim_id**: Victim player or NPC id.
* `number` **damage**: Damage to deal. Use [setEventValue](../../shared-functions/event/setEventValue.md)(newDamage) to change it, or
* `number` **damageType**: Gothic damage type/mode flags. For more information, see [Damage Constants](../../shared-constants/Damage.md).
