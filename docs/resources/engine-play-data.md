# Engine Play Data

Engine play data is used by Sonolus app to drive a level's gameplay.

## Resource Type

JSON resource.

`.json` is the only supported format, and must also be GZip compressed.

## Syntax

```ts
type EnginePlayData = {
    skin: {
        sprites: {
            name: SkinSpriteName | (string & {})
            id: number
        }[]
    }
    effect: {
        clips: {
            name: EffectClipName | (string & {})
            id: number
        }[]
    }
    particle: {
        effects: {
            name: ParticleEffectName | (string & {})
            id: number
        }[]
    }
    buckets: EngineDataBucket[]
    archetypes: EnginePlayDataArchetype[]
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
