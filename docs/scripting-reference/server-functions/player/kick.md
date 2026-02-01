---
title: 'kick'
---
# `function` kick <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    The reason string can't be longer than 255 characters.

Kick the player from the server.

## Declaration
```cpp
void kick(int player_id, string reason)
```

## Parameters
* `int` **player_id**: Target player id.
* `string` **reason**: Optional reason why the player was kicked.
