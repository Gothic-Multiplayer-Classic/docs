---
title: 'ban'
---
# `function` ban <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    The reason string can't be longer than 255 characters.

This function will ban the player on the server.

## Declaration
```cpp
void ban(int player_id, string reason)
```

## Parameters
* `int` **player_id**: Target player id.
* `string` **reason**: Optional reason why the player was banned.
