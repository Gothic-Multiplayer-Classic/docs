---
title: 'onPlayerChangeHealth'
---
# `event` onPlayerChangeHealth <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when player health changes.

## Parameters
```c++
void onPlayerChangeHealth(int player_id, int oldHP, int newHP)
```

* `int` **player_id**: The id of the player whose health points got changed.
* `int` **oldHP**: The previous health points of the player.
* `int` **newHP**: The new health points of the player.
