---
title: 'Route'
---
# `class` Route <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a route between two waypoint names computed from Zengin zCRoute class.

### Constructor
```cpp
Route.new(string startWp, string endWp)
```

**Parameters:**

* `string` **startWp**: Name of the start waypoint.
* `string` **endWp**: Name of the end waypoint.

## Properties
No properties.

----

## Methods
### getStart

This method will return the start waypoint name.

```cpp
string getStart()
```

  
**Returns `string`:**



----
### getEnd

This method will return the end waypoint name.

```cpp
string getEnd()
```

  
**Returns `string`:**



----
### getWaypointCount

This method will return the number of waypoints in the computed route.

```cpp
number getWaypointCount()
```

  
**Returns `number`:**

Number of waypoints.

----
### getWaypointNames

Returns a one-based Lua array of waypoint names.

```cpp
table getWaypointNames()
```

  
**Returns `table`:**

Waypoint names.

----

## Callbacks
No callbacks.

----
