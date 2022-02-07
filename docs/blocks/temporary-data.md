# Temporary Data

Temporary Data block is used to provide temporary information during callbacks.

## Identifier

```ts
const TemporaryDataId = 101
```

## Values

### `touch` Callback

| Index | Initial Value | Description                                                   |
| ----- | ------------- | ------------------------------------------------------------- |
| 0     | ?             | Touch identifier                                              |
| 1     | ?             | Touch started: `1` = Yes, `0` = No                            |
| 2     | ?             | Touch ended: `1` = Yes, `0` = No                              |
| 3     | ?             | Touch t: time of touch event reported by operating system     |
| 4     | ?             | Touch st: start time of touch reported by operating system    |
| 5     | ?             | Touch x: x of touch's current position                        |
| 6     | ?             | Touch y: y of touch's current position                        |
| 7     | ?             | Touch sx: x of touch's starting position                      |
| 8     | ?             | Touch sy: y of touch's starting position                      |
| 9     | ?             | Touch dx: delta x of touch's position since last update cycle |
| 10    | ?             | Touch dy: delta y of touch's position since last update cycle |
| 11    | ?             | Touch vx: x of touch's velocity                               |
| 12    | ?             | Touch vy: y of touch's velocity                               |
| 13    | ?             | Touch vr: r of touch's velocity                               |
| 14    | ?             | Touch vw: w of touch's velocity                               |

## Access

| Callback           | Read | Write |
| ------------------ | :--: | :---: |
| `preprocess`       |      |       |
| `spawnOrder`       |      |       |
| `shouldSpawn`      |      |       |
| `initialize`       |      |       |
| `updateSequential` |      |       |
| `touch`            |  ✔   |  ❌   |
| `updateParallel`   |      |       |
| `terminate`        |      |       |
