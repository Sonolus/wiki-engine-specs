# Entity Input

Entity Input block is used by entities to pass input information back to Sonolus.

## Identifier

```ts
const EntityInputId = 4004
```

## Values

| Index | Initial Value | Description               |
| ----- | ------------- | ------------------------- |
| 0     | 0             | Target time of the entity |

## Access

| Callback           | Read | Write |
| ------------------ | :--: | :---: |
| `preprocess`       |  ✔   |   ✔   |
| `spawnTime`        |  ✔   |   ✔   |
| `despawnTime`      |  ✔   |   ✔   |
| `initialize`       |  ✔   |   ✔   |
| `updateSequential` |  ✔   |   ✔   |
| `updateParallel`   |  ✔   |   ✔   |
| `terminate`        |  ✔   |   ✔   |
| `updateSpawn`      |  ✔   |  ❌   |

## Remarks

For entities spawned by `Spawn` function call, it does not have any data and cannot access this block.
