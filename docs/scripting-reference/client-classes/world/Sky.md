---
title: 'Sky'
---
# `class` Sky <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Static sky controller for local and synchronized sky settings.


## Properties
### `number` weatherType 

Current local weather type. Use `requestTimeAndSkySync` to pull the authoritative value from the server. For more
information, see [Weather Constants](../../shared-constants/Weather.md).

----
### `table` rainStartTime 

Rain start time: `{hour = number, minute = number}`

----
### `table` rainStopTime 

Rain stop time: `{hour = number, minute = number}`

----
### `number` windScale 

Wind scale used during precipitation.

----
### `boolean` precipitationEnabled 

Toggles local rain and snow rendering.

----

## Methods
### setFogColor

Sets one local fog color entry to the supplied RGB color.

```cpp
void setFogColor(number id, table value)
```

**Parameters:**

* `number` **id**: Fog entry or sky planet id.
* `table` **value**: RGB table {r, g, b}.
  

----
### setCloudsColor

Sets the local cloud RGB color.

```cpp
void setCloudsColor(table value)
```

**Parameters:**

* `table` **value**: RGB table {r, g, b}.
  

----
### setPlanetSize

Sets the size of one sky planet.

```cpp
void setPlanetSize(number id, number size)
```

**Parameters:**

* `number` **id**: Fog entry or sky planet id.
* `number` **size**: Planet size.
  

----
### setPlanetColor

Sets one sky planet RGBA color.

```cpp
void setPlanetColor(number id, table value)
```

**Parameters:**

* `number` **id**: Fog entry or sky planet id.
* `table` **value**: RGBA table {r, g, b, a}.
  

----
### setPlanetTexture

Sets the texture file of one sky planet.

```cpp
void setPlanetTexture(number id, string file)
```

**Parameters:**

* `number` **id**: Fog entry or sky planet id.
* `string` **file**: Texture file name.
  

----
### setLightingColor

Sets the local sky lighting RGB color.

```cpp
void setLightingColor(table value)
```

**Parameters:**

* `table` **value**: RGB table {r, g, b}.
  

----
### requestTimeAndSkySync

Requests authoritative time and sky settings; they are applied asynchronously when the reply arrives.

```cpp
boolean requestTimeAndSkySync()
```

  
**Returns `boolean`:**

Whether the request was sent; completion is asynchronous.

----

## Callbacks
No callbacks.

----
