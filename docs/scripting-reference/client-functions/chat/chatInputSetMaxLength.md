---
title: 'chatInputSetMaxLength'
---
# `function` chatInputSetMaxLength <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function changes the maximum chat input length in bytes.
The native default is 84 bytes.
The length is clamped to 1-1024, matching the message packet limit.
Existing text is truncated and the caret is clamped when necessary.

## Declaration
```cpp
void chatInputSetMaxLength(number length)
```

## Parameters
* `number` **length**: Maximum input length.
