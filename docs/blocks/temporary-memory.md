# Temporary Memory

Temporary Memory block is used to provide temporary operational memory during callbacks.

## Identifier

```ts
const TemporaryMemoryId = 100
```

## Values

### `touch` Callback

| Index | Initial Value | Description    |
| ----- | ------------- | -------------- |
| 0-15  | 0             | Generic memory |

## Access

| Callback           | Read | Write |
| ------------------ | :--: | :---: |
| `preprocess`       |      |       |
| `spawnOrder`       |      |       |
| `shouldSpawn`      |      |       |
| `initialize`       |      |       |
| `updateSequential` |      |       |
| `touch`            |  ✔   |   ✔   |
| `updateParallel`   |      |       |
| `terminate`        |      |       |

## Remarks

During `touch` callback, for every new touch, values are reset to initial values.
