# `Spawn`

Spawn an entity with attached script and data injected into Entity Memory.

## Arguments

| Argument | Description       |
| -------- | ----------------- |
| id       | Script identifier |
| data     | Data to inject    |

## Return

`0`.

## Remarks

Entity is not spawned immediately, rather it is placed in the queue and spawned on next update cycle's spawning system.

Entity spawned by `Spawn` function call:

-   does not have an archetype, thus it cannot be a playable entity.
-   does not exist in Entity Info block.
-   does not have Entity Data, Entity Input, or Entity Shared Memory blocks.
