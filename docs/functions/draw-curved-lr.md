# `DrawCurvedLR`

Draw a skin sprite with curved edges.

## Arguments

| Argument | Description                      |
| -------- | -------------------------------- |
| id       | Sprite identifier                |
| x1       | X1                               |
| y1       | Y1                               |
| x2       | X2                               |
| y2       | Y2                               |
| x3       | X3                               |
| y3       | Y3                               |
| x4       | X4                               |
| y4       | Y4                               |
| z        | Z                                |
| a        | Alpha                            |
| n        | Number of segments               |
| cxL      | X of control point on left edge  |
| cyL      | Y of control point on left edge  |
| cxR      | X of control point on right edge |
| cyR      | Y of control point on right edge |

## Return

`0`.

## Remarks

Points are in the order of bottom-left, top-left, top-right, bottom-right.

Bézier curves are drawn on the curved edges with respective vertexes and control point.

Curved edges are drawn in segments. The bigger the number of segments, the smoother the curve, and the costlier the drawing.
