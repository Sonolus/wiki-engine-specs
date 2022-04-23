# Level Data

Level Data block contains level wide information.

## Identifier

```ts
const LevelDataId = 1
```

## Values

| Index  | Initial Value | Description                              |
| ------ | ------------- | ---------------------------------------- |
| 0      | ?             | Current time, updated every update cycle |
| 1      | ?             | Delta time, updated every update cycle   |
| 2      | ?             | Screen aspect ratio                      |
| 3      | ?             | Audio offset                             |
| 4      | ?             | Input offset                             |
| 5      | ?             | Render scale                             |
| 6      | ?             | Anti-aliasing                            |
| 7-4095 | 0             | Unused                                   |

## Access

| Callback           | Read | Write |
| ------------------ | :--: | :---: |
| `preprocess`       |  ✔   |   ✔   |
| `spawnOrder`       |  ✔   |   ✔   |
| `shouldSpawn`      |  ✔   |  ❌   |
| `initialize`       |  ✔   |  ❌   |
| `updateSequential` |  ✔   |  ❌   |
| `touch`            |  ✔   |  ❌   |
| `updateParallel`   |  ✔   |  ❌   |
| `terminate`        |  ✔   |  ❌   |
