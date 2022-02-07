# Engine Data Node

Engine data Node is used by scripts to execute logic.

## Syntax

```ts
type EngineDataNode = EngineDataValueNode | EngineDataFunctionNode

type EngineDataValueNode = {
    value: number
}

type EngineDataFunctionNode = {
    func: EngineDataFunctionName
    args: number[]
}

type EngineDataFunctionName =
    | 'Constant'
    | 'Execute'
    | 'Execute0'
    | 'If'
    | 'Switch'
    | 'SwitchWithDefault'
    | 'SwitchInteger'
    | 'SwitchIntegerWithDefault'
    | 'While'
    | 'Add'
    | 'Subtract'
    | 'Multiply'
    | 'Divide'
    | 'Mod'
    | 'Power'
    | 'Log'
    | 'Equal'
    | 'NotEqual'
    | 'Greater'
    | 'GreaterOr'
    | 'Less'
    | 'LessOr'
    | 'And'
    | 'Or'
    | 'Not'
    | 'Abs'
    | 'Sign'
    | 'Min'
    | 'Max'
    | 'Ceil'
    | 'Floor'
    | 'Round'
    | 'Frac'
    | 'Trunc'
    | 'Degree'
    | 'Radian'
    | 'Sin'
    | 'Cos'
    | 'Tan'
    | 'Sinh'
    | 'Cosh'
    | 'Tanh'
    | 'Arcsin'
    | 'Arccos'
    | 'Arctan'
    | 'Arctan2'
    | 'Clamp'
    | 'Lerp'
    | 'LerpClamped'
    | 'Unlerp'
    | 'UnlerpClamped'
    | 'Remap'
    | 'RemapClamped'
    | 'Smoothstep'
    | 'Random'
    | 'RandomInteger'
    | 'Get'
    | 'GetShifted'
    | 'Set'
    | 'SetShifted'
    | 'Draw'
    | 'DrawCurvedL'
    | 'DrawCurvedR'
    | 'DrawCurvedLR'
    | 'DrawCurvedB'
    | 'DrawCurvedT'
    | 'DrawCurvedBT'
    | 'Play'
    | 'PlayScheduled'
    | 'Spawn'
    | 'SpawnParticleEffect'
    | 'MoveParticleEffect'
    | 'DestroyParticleEffect'
    | 'HasSkinSprite'
    | 'HasEffectClip'
    | 'HasParticleEffect'
    | 'Judge'
    | 'JudgeSimple'
    | `Ease${'In' | 'Out' | 'InOut' | 'OutIn'}${
          | 'Sine'
          | 'Quad'
          | 'Cubic'
          | 'Quart'
          | 'Quint'
          | 'Expo'
          | 'Circ'
          | 'Back'
          | 'Elastic'}`
    | 'IsDebug'
    | 'DebugPause'
    | 'DebugLog'
```

### `args`

Indexes of argument nodes in `nodes` array.

## Example

```json
{
    "func": "Add",
    "args": [1, 2]
}
```

This is an `Add` function node that adds two argument nodes, which are index `1` and `2` in `nodes` array.
