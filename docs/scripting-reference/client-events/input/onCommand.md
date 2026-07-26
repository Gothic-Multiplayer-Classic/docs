---
title: 'onCommand'
---
# `event` onCommand <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a slash command is submitted through chat input.

## Parameters
```c++
void onCommand(string command, string params)
```

* `string` **command**: Command name without the leading slash.
* `string` **params**: Raw command parameters after the command name.
