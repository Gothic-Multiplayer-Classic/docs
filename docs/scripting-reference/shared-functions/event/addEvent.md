---
title: 'addEvent'
---
# `function` addEvent <font size="4">(shared-side)</font>

Registers a custom event. On the server, the current resource owns it and its handlers.

## Declaration
```cpp
boolean addEvent(string event_name, boolean|nil allow_remote_trigger)
```

## Parameters
* `string` **event_name**: Unique event name.
* `boolean|nil` **allow_remote_trigger**: Whether peers may send this event; false by default.
  
## Returns `boolean`
True if registered.
