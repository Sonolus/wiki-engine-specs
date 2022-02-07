# Engine Data

Engine data is used by Sonolus app to drive a level's gameplay.

## Syntax

```ts
type EngineData = {
    buckets: EngineDataBucket[]
    archetypes: EngineDataArchetype[]
    scripts: EngineDataScript[]
    nodes: EngineDataNode[]
}
```

## Examples

```json
{
    "buckets": [
        // ...
    ],
    "archetypes": [
        // ...
    ],
    "scripts": [
        // ...
    ],
    "nodes": [
        // ...
    ]
}
```
