---
title: 'onPlayerMessage'
---
# `event` onPlayerMessage <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a chat message is received locally.

## Parameters
```c++
void onPlayerMessage(number sender_id, number r, number g, number b, string message)
```

* `number` **sender_id**: Optional sender id (nil for system).
* `number` **r**: Red color component.
* `number` **g**: Green color component.
* `number` **b**: Blue color component.
* `string` **message**: Message text.
