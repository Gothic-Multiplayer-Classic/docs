---
title: 'Sky'
---
# `class` Sky <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Static sky controller for local and synchronized sky settings.


## Properties
### `number` weatherType 

Current local weather type. Use `refresh()` to pull the authoritative value from the server.

----
### `table` rainStartTime 

Rain start time: `{hour = number, min = number}`

----
### `table` rainStopTime 

Rain stop time: `{hour = number, min = number}`

----
### `number` windScale 

Wind scale used during precipitation.

----
### `boolean` dontRain 

Toggles local rain and snow rendering.

----
### `table` fogColor 

Write-only fog color table: `{id = number, r = number, g = number, b = number}`

----
### `table` cloudsColor 

Write-only cloud color table: `{r = number, g = number, b = number}`

----
### `table` planetSize 

Write-only planet size table: `{planetId = number, size = number}`

----
### `table` planetColor 

Write-only planet color table: `{planetId = number, r = number, g = number, b = number, a = number}`

----
### `table` planetTxt 

Write-only planet texture table: `{planetId = number, texture = string}`

----
### `table` lightingColor 

Write-only lighting color table: `{r = number, g = number, b = number}`

----

## Methods
### refresh

Requests authoritative time and sky settings from the server and applies them when the reply arrives.

```cpp
boolean refresh()
```

  
**Returns `boolean`:**

True if the refresh request was sent.

----

## Callbacks
No callbacks.

----
