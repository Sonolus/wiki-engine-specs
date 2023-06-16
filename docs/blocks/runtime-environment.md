# Runtime Environment

Runtime Environment block contains runtime environment information.

## Identifier

```ts
const RuntimeEnvironmentId = 1000
```

## Values

| Index | Initial Value | Description                     |
| ----- | ------------- | ------------------------------- |
| 0     | ?             | Debug mode: `1` = Yes, `0` = No |
| 1     | ?             | Screen aspect ratio             |
| 2     | ?             | Audio offset                    |
| 3     | ?             | Input offset                    |

## Access

| Callback           | Read | Write |
| ------------------ | :--: | :---: |
| `preprocess`       |  ✔   |   ✔   |
| `spawnOrder`       |  ✔   |  ❌   |
| `shouldSpawn`      |  ✔   |  ❌   |
| `initialize`       |  ✔   |  ❌   |
| `updateSequential` |  ✔   |  ❌   |
| `touch`            |  ✔   |  ❌   |
| `updateParallel`   |  ✔   |  ❌   |
| `terminate`        |  ✔   |  ❌   |
