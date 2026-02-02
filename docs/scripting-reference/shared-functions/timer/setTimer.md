---
title: 'setTimer'
---
# `function` setTimer <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Create a new timer that calls the given function at a fixed interval.

The timer passes any additional arguments to the callback when it executes.
If execute_times is 0 or negative, the timer repeats indefinitely.

## Declaration
```cpp
number setTimer(function func, number interval, number execute_times, ... ...)
```

## Parameters
* `function` **func**: Callback function executed by the timer.
* `number` **interval**: Interval in milliseconds.
* `number` **execute_times**: How many times to execute the callback (<= 0 means infinite).
* `...` **...**: Additional arguments forwarded to the callback.
  
## Returns `number`
Timer ID.
