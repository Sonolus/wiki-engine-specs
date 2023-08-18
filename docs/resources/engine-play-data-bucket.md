# Engine Play Data Bucket

Engine play data bucket is used by Sonolus app to populate judgment graphs in result screen.

## Syntax

```ts
type EnginePlayDataBucket = {
    sprites: EnginePlayDataBucketSprite[]
    unit?: UnitText | (string & {})
}

type EnginePlayDataBucketSprite = {
    id: number
    fallbackId?: number
    x: number
    y: number
    w: number
    h: number
    rotation: number
}
```

## Examples

```json
{
    "sprites": [
        {
            "id": 0,
            "fallbackId": 1,
            "x": 0,
            "y": 0,
            "w": 2,
            "h": 2,
            "rotation": 0
        }
    ],
    "unit": "#MILLISECOND"
}
```
