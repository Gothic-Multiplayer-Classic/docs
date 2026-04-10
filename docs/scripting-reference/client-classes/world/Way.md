---
title: 'Way'
---
# `class` Way <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"



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
### getWaypoints

Get all waypoints from the computed route.

```cpp
[wpName...] getWaypoints()
```

  
**Returns `[wpName...]`:**

Array with waypoint names.

----
### getCountWaypoints

Get number of waypoints in the computed route.

```cpp
number getCountWaypoints()
```

  
**Returns `number`:**



----

## Callbacks
No callbacks.

----
