# Engine Data

Engine data is used by Sonolus app to drive a level's gameplay.

## Syntax

```ts
type EngineData = {
    skin: {
        sprites: {
            name: string
            id: number
        }[]
    }
    effect: {
        clips: {
            name: string
            id: number
        }[]
    }
    particle: {
        effects: {
            name: string
            id: number
        }[]
    }
    buckets: EngineDataBucket[]
    archetypes: EngineDataArchetype[]
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
    "effect": {
        "clips": [
            {
                "name": "#PERFECT",
                "id": 0
            }
        ]
    },
    "particle": {
        "effects": [
            {
                "name": "#NOTE_CIRCULAR_TAP_CYAN",
                "id": 0
            }
        ]
    },
    "buckets": [
        // ...
    ],
    "archetypes": [
        // ...
    ],
    "nodes": [
        // ...
    ]
}
```
