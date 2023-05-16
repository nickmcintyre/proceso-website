# quad

`quad()`

## Description

Draws a quad on the canvas. A quad is a quadrilateral, a four-sided polygon.
It is similar to a rectangle, but the angles between its edges are not
constrained to ninety degrees. The first pair of parameters (x1, y1) sets
the first vertex and the subsequent pairs should proceed clockwise or
counter-clockwise around the defined shape. z-arguments only work when
`quad()` is used in WEBGL mode.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Irregular white quadrilateral with black outline")

p5.quad(38, 31, 86, 20, 69, 63, 30, 76)
```

## Syntax

`quad(x1, y1, x2, y2, x3, y3, x4, y4, [detail_x], [detail_y])`

`quad(x1, y1, z1, x2, y2, z2, x3, y3, z3, x4, y4, z4, [detail_x], [detail_y])`

## Parameters

`x1: float` x-coordinate of the first point.

`y1: float` y-coordinate of the first point.

`x2: float` x-coordinate of the second point.

`y2: float` y-coordinate of the second point.

`x3: float` x-coordinate of the third point.

`y3: float` y-coordinate of the third point.

`x4: float` x-coordinate of the fourth point.

`y4: float` y-coordinate of the fourth point.

`[detail_x]: int` Number of segments in the x-direction.

`[detail_y]: int` Number of segments in the y-direction.

`z1: float` z-coordinate of the first point.

`z2: float` z-coordinate of the second point.

`z3: float` z-coordinate of the third point.

`z4: float` z-coordinate of the fourth point.
