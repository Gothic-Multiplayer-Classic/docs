---
title: 'getTimerInterval'
---
# `function` getTimerInterval <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the interval (in milliseconds) of a timer, or nil if the timer does not exist.

## Declaration
```cpp
number|nil getTimerInterval(number timer_id)
```

## Parameters
* `number` **timer_id**: Timer ID returned by setTimer.
  
## Returns `number|nil`
Interval in milliseconds, or nil if not found.
