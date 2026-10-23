---
title: 'callEvent'
---
# `function` callEvent <font size="4">(shared-side)</font>

Dispatches a local custom event. Handlers receive (context, ...); payload arguments are never interpreted as metadata.

## Declaration
```cpp
boolean callEvent(string name, table|nil options, any... ...)
```

## Parameters
* `string` **name**: Custom event registered with [addEvent](addEvent.md).
* `table|nil` **options**: Metadata {sourceId = positive integer}; pass nil for no metadata.
* `any...` **...**: Payload arguments, passed unchanged and in order, including nil.
  
## Returns `boolean`
True if dispatched and not cancelled.
