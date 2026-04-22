---
title: 'onPlayerHit'
---
# `event` onPlayerHit <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player is hit.

## Parameters
```c++
void onPlayerHit(number attacker_id, number victim_id, number damage)
```

* `number` **attacker_id**: Optional attacker id (nil if none).
* `number` **victim_id**: Victim player id.
* `number` **damage**: Damage dealt.
