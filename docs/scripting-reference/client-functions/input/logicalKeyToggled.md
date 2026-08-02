---
title: 'logicalKeyToggled'
---
# `function` logicalKeyToggled <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will check whether the specified Gothic logical game action was toggled from unpressed to pressed state.

## Declaration
```cpp
boolean logicalKeyToggled(number key)
```

## Parameters
* `number` **key**: The logical game action code to check. For more information, see [Logical Key Constants](../../client-constants/LogicalKey.md).
  
## Returns `boolean`
True if the logical action became pressed this frame, false otherwise.
