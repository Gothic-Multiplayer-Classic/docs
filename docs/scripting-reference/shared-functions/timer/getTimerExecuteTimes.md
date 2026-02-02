---
title: 'getTimerExecuteTimes'
---
# `function` getTimerExecuteTimes <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Return how many times the timer will execute, or nil if the timer does not exist.

A value of 0 means the timer repeats indefinitely.

## Declaration
```cpp
number|nil getTimerExecuteTimes(number timer_id)
```

## Parameters
* `number` **timer_id**: Timer ID returned by setTimer.
  
## Returns `number|nil`
Execute count (0 = infinite), or nil if not found.
