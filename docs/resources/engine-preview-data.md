# Engine Preview Data

Engine preview data is used by Sonolus app to drive a level's preview.

## Resource Type

JSON resource.

`.json` is the only supported format, and must also be GZip compressed.

## Syntax

```ts
type EnginePreviewData = {
    skin: {
        sprites: {
            name: SkinSpriteName | (string & {})
            id: number
        }[]
    }
    archetypes: EnginePreviewDataArchetype[]
    nodes: EngineDataNode[]
}
```

## Examples

```json
{
    "skin": {
        "sprites": [
            {
                "name": "#NOTE_HEAD_CYAN",
                "id": 0
            }
        ]
    },
    "archetypes": [
        // ...
    ],
    "nodes": [
        // ...
    ]
}
```
