# circle

`circle()`

## Description



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
