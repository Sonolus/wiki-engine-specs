# Runtime UI

Runtime UI block is used to pass UI layout information back to Sonolus.

## Identifier

```ts
const RuntimeUIId = 1003
```

## Values

| Index | Initial Value | Description                   |
| ----- | ------------- | ----------------------------- |
| 0-8   | 0             | Layout information of menu UI |

For each UI:

| Index         | Initial Value | Description |
| ------------- | ------------- | ----------- |
| UI offset + 0 | 0             | Anchor X    |
| UI offset + 1 | 0             | Anchor Y    |
| UI offset + 2 | 0             | Pivot X     |
| UI offset + 3 | 0             | Pivot Y     |
| UI offset + 4 | 0             | Width       |
| UI offset + 5 | 0             | Height      |
| UI offset + 6 | 0             | Rotation    |
| UI offset + 7 | 0             | Alpha       |
| UI offset + 8 | 0             | Background  |

## Access

| Callback     | Read | Write |
| ------------ | :--: | :---: |
| `preprocess` |  ✔   |   ✔   |
| `render`     |  ✔   |  ❌   |

## Remarks

It is recommended to adjust UI layout based on various factors such as screen aspect ratio and Runtime UI Configuration.
