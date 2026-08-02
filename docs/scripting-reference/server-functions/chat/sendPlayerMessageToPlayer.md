---
title: 'sendPlayerMessageToPlayer'
---
# `function` sendPlayerMessageToPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will send a player-sourced colored message to a specific player.

## Declaration
```cpp
boolean sendPlayerMessageToPlayer(number sender_id, number receiver_id, number r, number g, number b, string text)
```

## Parameters
* `number` **sender_id**: Sender player id.
* `number` **receiver_id**: Receiver player id.
* `number` **r**: Red component (0-255).
* `number` **g**: Green component (0-255).
* `number` **b**: Blue component (0-255).
* `string` **text**: Message text.
  
## Returns `boolean`
True on success.
