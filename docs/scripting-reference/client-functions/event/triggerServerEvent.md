---
title: 'triggerServerEvent'
---
# `function` triggerServerEvent <font size="4">(client-side)</font>

Sends payload arguments to a remote-enabled server event. The server supplies context.senderPlayerId from the authenticated connection,
independently of payload and sourceId.

## Declaration
```cpp
boolean triggerServerEvent(string name, table|nil options, any... ...)
```

## Parameters
* `string` **name**: Remote-enabled server event name.
* `table|nil` **options**: Metadata {sourceId = positive integer}; pass nil for no metadata.
* `any...` **...**: Serializable payload arguments, including nil.
  
## Returns `boolean`
Whether the event was sent.
