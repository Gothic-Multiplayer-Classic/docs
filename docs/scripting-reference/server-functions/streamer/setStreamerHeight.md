---
title: 'setStreamerHeight'
---
# `function` setStreamerHeight <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function sets the global player streaming height. A value of 0 disables the vertical limit.

## Declaration
```cpp
boolean setStreamerHeight(number height)
```

## Parameters
* `number` **height**: Streaming height in world units, or 0 for unlimited.
  
## Returns `boolean`
True if the value was accepted.
