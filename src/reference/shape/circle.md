# circle

`circle()`

## Description

Draws a circle to the screen. A circle is a simple closed shape. It is the set
of all points in a plane that are at a given distance from a given point, the
center. This function is a special case of the `ellipse()` function, where the
width and height of the ellipse are the same. Height and width of the ellipse
correspond to the diameter of the circle. By default, the first two parameters
set the location of the center of the circle, the third sets the diameter of
the circle.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White circle with black outline in mid of gray canvas")

# Draw a circle at location (30, 30) with a diameter of 20.
p5.circle(30, 30, 20)
```

## Syntax

`circle(x, y, d)`

## Parameters

`x: float` x-coordinate of the center of the circle.

`y: float` y-coordinate of the center of the circle.

`d: float` Diameter of the circle.
