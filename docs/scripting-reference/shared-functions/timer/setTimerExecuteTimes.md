---
title: 'setTimerExecuteTimes'
---
# `function` setTimerExecuteTimes <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This function will set how many times the timer should execute.
If execute_times is 0 or negative, the timer repeats indefinitely.

## Declaration
```cpp
void setTimerExecuteTimes(number timer_id, number execute_times)
```

## Parameters
* `number` **timer_id**: Timer ID returned by setTimer.
* `number` **execute_times**: How many times to execute (<= 0 means infinite).
