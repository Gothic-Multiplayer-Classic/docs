---
title: 'getTimerRemainingExecutions'
---
# `function` getTimerRemainingExecutions <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This function will return how many times the timer will execute, or nil if the timer does not exist.
A value of 0 means the timer repeats indefinitely.

## Declaration
```cpp
number|nil getTimerRemainingExecutions(number timer_id)
```

## Parameters
* `number` **timer_id**: Timer ID returned by [setTimer](setTimer.md).
  
## Returns `number|nil`
Execute count (0 = infinite), or nil if not found.
