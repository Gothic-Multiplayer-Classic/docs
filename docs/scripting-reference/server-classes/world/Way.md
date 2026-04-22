---
title: 'Way'
---
# `class` Way <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Represents a route between two waypoint names computed from server-side waynet JSON.

### Constructor
```cpp
Way.new(string world, string startWp, string endWp)
```

**Parameters:**

* `string` **world**: World name (example: NEWWORLD\\NEWWORLD.ZEN).
* `string` **startWp**: Name of the start waypoint.
* `string` **endWp**: Name of the end waypoint.

## Properties
No properties.

----

## Methods
### getStart

Returns the start waypoint name.

```cpp
string getStart()
```

  
**Returns `string`:**



----
### getEnd

Returns the end waypoint name.

```cpp
string getEnd()
```

  
**Returns `string`:**



----
### getCountWaypoints

Returns number of waypoints in the computed path.

```cpp
number getCountWaypoints()
```

  
**Returns `number`:**



----
### getWaypoints

Returns all waypoint names in the computed path.

```cpp
[wpName...] getWaypoints()
```

  
**Returns `[wpName...]`:**



----

## Callbacks
No callbacks.

----
