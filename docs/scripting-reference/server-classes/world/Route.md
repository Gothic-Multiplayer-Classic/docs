---
title: 'Route'
---
# `class` Route <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Represents a complete route between two waypoint names computed from server-side waynet JSON data.

### Constructor
```cpp
Route.new(string world, string startWp, string endWp)
```

**Parameters:**

* `string` **world**: World name.
* `string` **startWp**: Start waypoint name.
* `string` **endWp**: End waypoint name.

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
### getWaypointCount

Returns the number of waypoint names in the route.

```cpp
number getWaypointCount()
```

  
**Returns `number`:**



----
### getWaypointNames

Returns a one-based array of waypoint names.

```cpp
table getWaypointNames()
```

  
**Returns `table`:**



----

## Callbacks
No callbacks.

----
