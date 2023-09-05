# Runtime UI Configuration

Runtime UI Configuration block contains configuration of preview UI elements.

## Identifier

```ts
const RuntimeUIConfigurationId = 1004
```

## Values

| Index | Initial Value | Description              |
| ----- | ------------- | ------------------------ |
| 0-1   | 0             | Configuration of menu UI |

For each UI:

| Index         | Initial Value | Description |
| ------------- | ------------- | ----------- |
| UI offset + 0 | 0             | Scale       |
| UI offset + 1 | 0             | Alpha       |

## Access

| Callback     | Read | Write |
| ------------ | :--: | :---: |
| `preprocess` |  ✔   |   ✔   |
| `render`     |  ✔   |  ❌   |
