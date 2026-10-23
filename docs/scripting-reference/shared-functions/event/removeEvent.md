---
title: 'removeEvent'
---
# `function` removeEvent <font size="4">(shared-side)</font>

Removes a custom event and its handlers. On the server, only its owning resource may remove it.

## Declaration
```cpp
void removeEvent(string event_name)
```

## Parameters
* `string` **event_name**: Custom event name.
