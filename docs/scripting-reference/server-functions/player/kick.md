---
title: 'kick'
---
# `function` kick <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    The reason string can't be longer than 255 characters.

This function will kick the player from the server.

## Declaration
```cpp
void kick(number player_id, string|nil reason)
```

## Parameters
* `number` **player_id**: Target player id.
* `string|nil` **reason**: Optional reason why the player was kicked.
