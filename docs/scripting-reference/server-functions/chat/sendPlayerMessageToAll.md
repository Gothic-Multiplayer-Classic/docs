---
title: 'sendPlayerMessageToAll'
---
# `function` sendPlayerMessageToAll <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Send a player-sourced colored message to all players (includes sender id).

## Declaration
```cpp
boolean sendPlayerMessageToAll(number sender_id, number r, number g, number b, string text)
```

## Parameters
* `number` **sender_id**: Sender player id.
* `number` **r**: Red component (0-255).
* `number` **g**: Green component (0-255).
* `number` **b**: Blue component (0-255).
* `string` **text**: Message text.
  
## Returns `boolean`
True on success, false if the sender is missing.
