---
title: 'onPlayerMessage'
---
# `event` onPlayerMessage <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a chat message is received locally.

## Parameters
```c++
void onPlayerMessage(number sender_id, number r, number g, number b, string message)
```

* `number` **sender_id**: Optional sender id (nil for system).
* `number` **r**: The red color component in RGB model.
* `number` **g**: The green color component in RGB model.
* `number` **b**: The blue color component in RGB model.
* `string` **message**: Message text.
