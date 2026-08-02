---
title: 'onPlayerUnconscious'
---
# `event` onPlayerUnconscious <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player becomes unconscious.

## Parameters
```c++
void onPlayerUnconscious(number|nil attacker_id, number victim_id)
```

* `number|nil` **attacker_id**: Optional attacker id (nil if none).
* `number` **victim_id**: Victim player id.
