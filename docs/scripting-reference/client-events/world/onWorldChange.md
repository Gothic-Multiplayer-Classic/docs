---
title: 'onWorldChange'
---
# `event` onWorldChange <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when the client requests a world change via oCTriggerChangeLevel vob.

## Parameters
```c++
void onWorldChange(string world, string waypoint)
```

* `string` **world**: New world filename.
* `string` **waypoint**: Waypoint name the player will be teleported to.
