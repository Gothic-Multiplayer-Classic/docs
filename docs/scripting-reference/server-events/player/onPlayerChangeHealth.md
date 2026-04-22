---
title: 'onPlayerChangeHealth'
---
# `event` onPlayerChangeHealth <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when player health changes.

## Parameters
```c++
void onPlayerChangeHealth(number player_id, number oldHP, number newHP)
```

* `number` **player_id**: The id of the player whose health points got changed.
* `number` **oldHP**: The previous health points of the player.
* `number` **newHP**: The new health points of the player.
