# Engine Configuration UI

Engine configuration UI is used by Sonolus app to populate UI section in level and engine configuration interface.

## Syntax

```ts
type EngineConfigurationUI = {
    scope?: string
    primaryMetric: EngineConfigurationMetric
    secondaryMetric: EngineConfigurationMetric
    menuVisibility: EngineConfigurationVisibility
    judgmentVisibility: EngineConfigurationVisibility
    comboVisibility: EngineConfigurationVisibility
    primaryMetricVisibility: EngineConfigurationVisibility
    secondaryMetricVisibility: EngineConfigurationVisibility
    judgmentAnimation: EngineConfigurationAnimation
    comboAnimation: EngineConfigurationAnimation
    judgmentErrorStyle: EngineConfigurationJudgmentErrorStyle
    judgmentErrorPlacement: EngineConfigurationJudgmentErrorPlacement
    judgmentErrorMin: number
}

type EngineConfigurationMetric = 'arcade' | 'accuracy' | 'life' | 'perfectRate' | 'errorHeatmap'

type EngineConfigurationVisibility = {
    scale: number
    alpha: number
}

type EngineConfigurationAnimation = {
    scale: EngineConfigurationAnimationTween
    alpha: EngineConfigurationAnimationTween
}

type EngineConfigurationAnimationTween = {
    from: number
    to: number
    duration: number
    ease:
        | 'Linear'
        | `${'In' | 'Out' | 'InOut' | 'OutIn'}${
              | 'Sine'
              | 'Quad'
              | 'Cubic'
              | 'Quart'
              | 'Quint'
              | 'Expo'
              | 'Circ'
              | 'Back'
              | 'Elastic'}`
        | 'None'
}

type EngineConfigurationJudgmentErrorStyle =
    | 'none'
    | 'plus'
    | 'minus'
    | 'arrowUp'
    | 'arrowDown'
    | 'arrowLeft'
    | 'arrowRight'
    | 'triangleUp'
    | 'triangleDown'
    | 'triangleLeft'
    | 'triangleRight'

type EngineConfigurationJudgmentErrorPlacement = 'both' | 'left' | 'right'
```

### `scope`

UI values are automatically saved and shared between all engines. When a saved value matching the scope exists, it will be recalled.

Without specifying a scope, UI values will be saved only for this engine.

## Example

```json
{
    "scope": "ExampleEngine",
    "primaryMetric": "arcade",
    "secondaryMetric": "life",
    "menuVisibility": {
        "scale": 1,
        "alpha": 1
    },
    "judgmentVisibility": {
        "scale": 1,
        "alpha": 1
    },
    "comboVisibility": {
        "scale": 1,
        "alpha": 1
    },
    "primaryMetricVisibility": {
        "scale": 1,
        "alpha": 1
    },
    "secondaryMetricVisibility": {
        "scale": 1,
        "alpha": 1
    },
    "judgmentAnimation": {
        "scale": {
            "from": 1,
            "to": 1,
            "duration": 0,
            "ease": "Linear"
        },
        "alpha": {
            "from": 1,
            "to": 0,
            "duration": 0.2,
            "ease": "InQuart"
        }
    },
    "comboAnimation": {
        "scale": {
            "from": 1.2,
            "to": 1,
            "duration": 0.2,
            "ease": "InBack"
        },
        "alpha": {
            "from": 1,
            "to": 1,
            "duration": 0,
            "ease": "Linear"
        }
    },
    "judgmentErrorStyle": "arrowDown",
    "judgmentErrorPlacement": "both",
    "judgmentErrorMin": 20
}
```
