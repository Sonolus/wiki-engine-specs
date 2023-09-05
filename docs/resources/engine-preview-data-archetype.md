# Engine Preview Data Archetype

Engine preview data archetype is used by level to populate entities in preview mode.

## Syntax

```ts
type EnginePreviewDataArchetype = {
    name: EngineArchetypeName | (string & {})
    preprocess?: EnginePreviewDataArchetypeCallback
    render?: EnginePreviewDataArchetypeCallback
    data: {
        name: EngineArchetypeDataName | (string & {})
        index: number
    }[]
}

type EnginePreviewDataArchetypeCallback = {
    index: number
    order?: number
}
```

### `name`

Name of this archetype, which will be referenced by entities in level data.

### `data`

Entity data to be inject into Entity Data block.

Entity data with matching `name` will be injected at `index` of Entity Data block.

### `EnginePreviewDataArchetypeCallback.index`

Index of entry node in `nodes` array.

## Example

```json
{
    "name": "TapNote",
    "preprocess": {
        "index": 0,
        "order": 0
    },
    "data": [
        {
            "name": "#BEAT",
            "index": 0
        }
    ]
}
```
