---
title: 'create'
---
# `function` create <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Creates a synchronized ground item.

## Declaration
```cpp
number create({...} options, string options.instance, number options.amount, boolean options.physicsEnabled, {x, y, z} options.position, {x, y, z} options.rotation, string options.world, number options.virtualWorld)
```

## Parameters
* `{...}` **options**: Creation options.
* `string` **options.instance**: Gothic item instance name.
* `number` **options.amount**: Optional amount. Defaults to 1.
* `boolean` **options.physicsEnabled**: Optional physics flag. Defaults to false.
* `{x, y, z}` **options.position**: Optional world position. Defaults to 0,0,0.
* `{x, y, z}` **options.rotation**: Optional Euler rotation. Defaults to 0,0,0.
* `string` **options.world**: Optional world name. Defaults to the server world.
* `number` **options.virtualWorld**: Optional virtual world id. Defaults to 0.
  
## Returns `number`
Ground item id, or 0 on failure.
