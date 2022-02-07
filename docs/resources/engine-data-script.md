# Engine Data Script

Engine data script is used by archetypes and entities spawned by `Spawn` function call to perform logic.

## Syntax

```ts
type EngineDataScript = {
    preprocess?: EngineDataScriptCallback
    spawnOrder?: EngineDataScriptCallback
    shouldSpawn?: EngineDataScriptCallback
    initialize?: EngineDataScriptCallback
    updateSequential?: EngineDataScriptCallback
    touch?: EngineDataScriptCallback
    updateParallel?: EngineDataScriptCallback
    terminate?: EngineDataScriptCallback
}

type EngineDataScriptCallback = {
    index: number
    order?: number
}
```

### `index`

Index of entry node in `nodes` array.

## Example

```json
{
    "preprocess": {
        "index": 0,
        "order": 0
    }
    // ...
}
```
