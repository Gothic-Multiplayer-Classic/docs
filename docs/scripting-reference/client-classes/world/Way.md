---
title: 'Way'
---
# `class` Way <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class represents a route between two waypoint names computed from Zengin zCRoute class.

### Constructor
```cpp
Way.new(string startWp, string endWp)
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
### getWaypoints

This method will return all waypoints from the computed route.

```cpp
{wpName...} getWaypoints()
```

  
**Returns `{wpName...}`:**

Table with waypoint names.

----
### getCountWaypoints

This method will return the number of waypoints in the computed route.

```cpp
number getCountWaypoints()
```

  
**Returns `number`:**

Number of waypoints.

----

## Callbacks
No callbacks.

----
