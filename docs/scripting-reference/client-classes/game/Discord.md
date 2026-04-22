---
title: 'Discord'
---
# `class` Discord <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This class exposes static methods for updating the user's Discord activity from the game client.


## Properties
No properties.

----

## Methods
### `static` setActivity

This function updates the Discord Rich Presence activity. Missing fields keep their last-set values.

```cpp
void setActivity({...} Activity)
```

**Parameters:**

* `{...}` **Activity**: configuration table.
  

----
### `static` setState

This function will update the activity state text.

```cpp
void setState(string state)
```

**Parameters:**

* `string` **state**: 
  

----
### `static` setDetails

This function will update the activity details text.

```cpp
void setDetails(string details)
```

**Parameters:**

* `string` **details**: 
  

----
### `static` setLargeImage

This function will update the large image entry for the activity.

```cpp
void setLargeImage(string key, string text)
```

**Parameters:**

* `string` **key**: Asset key for the large image.
* `string` **text**: Optional tooltip text for the large image.
  

----
### `static` setSmallImage

This function will update the small image entry for the activity.

```cpp
void setSmallImage(string key, string text)
```

**Parameters:**

* `string` **key**: Asset key for the small image.
* `string` **text**: Optional tooltip text for the small image.
  

----
### `static` clearActivity

This function will clear the current activity and stored values.

```cpp
void clearActivity()
```

  

----

## Callbacks
No callbacks.

----
