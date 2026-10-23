---
title: 'triggerClientEvent'
---
# `function` triggerClientEvent <font size="4">(server-side)</font>

Sends payload arguments to a client custom event. The server is the sender; options.sourceId is script metadata.

## Declaration
```cpp
boolean triggerClientEvent(number|table|nil recipients, string name, table|nil options, any... ...)
```

## Parameters
* `number|table|nil` **recipients**: Player id, array of player ids, or nil for all players.
* `string` **name**: Remote-enabled client event name.
* `table|nil` **options**: Metadata {sourceId = positive integer}; pass nil for no metadata.
* `any...` **...**: Serializable payload arguments, including nil.
  
## Returns `boolean`
Whether the event was sent.
