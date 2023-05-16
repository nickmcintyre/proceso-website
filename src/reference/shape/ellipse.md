# ellipse

`ellipse()`

## Description

Draws an ellipse (oval) to the screen. By default, the first two parameters
set the location of the center of the ellipse, and the third and fourth
parameters set the shape's width and height. If no height is specified, the
value of width is used for both the width and height. If a negative height or
width is specified, the absolute value is taken.

An ellipse with equal width and height is a circle. The origin may be
changed with the `ellipse_mode()` function.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White ellipse with black outline in middle of a gray canvas")

p5.ellipse(56, 46, 55, 55)
```

## Syntax

`ellipse(x, y, w, [h], [detail])`

## Parameters

`x: float` x-coordinate of the center of the ellipse.

`y: float` y-coordinate of the center of the ellipse.

`w: float` Width of the ellipse.

`[h]: float` Height of the ellipse.

`[detail]: int` Optional parameter for WEBGL mode only. This is to specify the number of vertices that makes up the perimeter of the ellipse. Default value is 25. Won't draw a stroke for a detail of more than 50.
