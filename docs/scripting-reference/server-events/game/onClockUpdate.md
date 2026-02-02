---
title: 'onClockUpdate'
---
# `event` onClockUpdate <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered every time the server clock updates.

## Parameters
```c++
void onClockUpdate(number day, number hour, number min)
```

* `number` **day**: The current ingame day.
* `number` **hour**: The current ingame hour.
* `number` **min**: The current ingame minute.
