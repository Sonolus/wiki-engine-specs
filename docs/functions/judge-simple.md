# `Judge`

Judge player timing.

## Arguments

| Argument | Description              |
| -------- | ------------------------ |
| target   | Target timing            |
| source   | Player timing            |
| max_1    | Maximum Perfect distance |
| max_2    | Maximum Great distance   |
| max_3    | Maximum Good distance    |

## Return

`1` if Perfect, `2` if Great, `3` if Good, and `0` otherwise.

## Remarks

It is the same as `Judge(target, source, -max1, max1, -max2, max2, -max3, max3)`.
