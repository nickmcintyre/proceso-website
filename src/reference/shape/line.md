# line

`line()`

## Description

Draws a line (a direct path between two points) to the screen.
If called with only 4 parameters, it will draw a line in 2D with a default
width of 1 pixel. This width can be modified by using the `stroke_weight()`
function. A line cannot be filled, therefore the `fill()` function will not
affect the color of a line. So to color a line, use the `stroke()` function.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "A line 78 pixels long running from top-center to bottom-right of canvas"
)

p5.line(30, 20, 85, 75)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "3 lines of various stroke colors. Form top, bottom and right sides of a square"
)

p5.line(30, 20, 85, 20)
p5.stroke(126)
p5.line(85, 20, 85, 75)
p5.stroke(255)
p5.line(85, 75, 30, 75)
```


## Syntax

`line(x1, y1, x2, y2)`

`line(x1, y1, z1, x2, y2, z2)`

## Parameters

`x1: float` x-coordinate of the first point.

`y1: float` y-coordinate of the first point.

`x2: float` x-coordinate of the second point.

`y2: float` y-coordinate of the second point.

`z1: float` z-coordinate of the first point.

`z2: float` z-coordinate of the second point.
