# `GetShifted`

Get a value from block.

## Arguments

| Argument | Description      |
| -------- | ---------------- |
| id       | Block identifier |
| i        | Index            |
| d        | Offset           |

## Return

Value at index i + d of the block id, or `0` if index is out of range or block does not exist.

## Remarks

It is the same as `Get(id, i + d)`.
