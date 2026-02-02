---
title: 'sendMessageToPlayer'
---
# `function` sendMessageToPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Send a colored chat message to a specific player.

## Declaration
```cpp
boolean sendMessageToPlayer(number player_id, number r, number g, number b, string text)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **r**: Red component (0-255).
* `number` **g**: Green component (0-255).
* `number` **b**: Blue component (0-255).
* `string` **text**: Message text to send.
  
## Returns `boolean`
True on success, false if the player is missing.
