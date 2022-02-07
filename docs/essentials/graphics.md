# Graphics

Essential topics related to graphics.

## Screen Coordinate

Sonolus uses a cardinal coordinate system with (0, 0) at center of the screen with 1 unit equals to half of screen height, and positive direction goes top/right of the screen.

This means `y = -1` to `y = 1` covers the whole screen height, and `x = -aspectRatio` to `x = aspectRatio` covers the whole screen width.

You can obtain screen aspect ratio from Level Data block.

## Z Value

Z value is used to order rendering of skin sprites.

Z value must be between 0 and 1000 in order for it to be rendered.

## Quad

Quad (quadrilateral) is the basic shape used in rendering. Points are in the order of bottom-left, top-left, top-right, bottom-right.

When rendering background texture, perspective interpolation is used to create 3D depth perception.

When rendering skin sprites by `Draw` function calls, bilinear interpolation is used to preserve 2D proportions.
