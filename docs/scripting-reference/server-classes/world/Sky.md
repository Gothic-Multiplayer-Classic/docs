---
title: 'Sky'
---
# `class` Sky <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Static sky controller for authoritative server weather.


## Properties
### `number` weatherType 

Current server weather type. When automatic weather is enabled, this can be overwritten on the next server game minute.

----
### `table` rainStartTime 

Rain start time: `{hour = number, min = number}`

----
### `table` rainStopTime 
!!! note
    The stop time must be after `rainStartTime` in Gothic sky time.

Rain stop time: `{hour = number, min = number}`

----
### `number` windScale 

Wind scale used during precipitation.

----
### `boolean` dontRain 

Disables rain and snow rendering while leaving automatic weather timing active.

----
### `boolean` disabled 

Toggles the server automatic weather state machine. Set this to true before manually controlling weather.

----

## Methods
No methods.

----

## Callbacks
No callbacks.

----
