# point

`point()`

## Description

Draws a point, a coordinate in space at the dimension of one pixel.
The first parameter is the horizontal value for the point, the second
param is the vertical value for the point. The color of the point is
changed with the `stroke()` function. The size of the point can be changed
with the `stroke_weight()` function.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("4 points create the corners of a square")

p5.point(30, 20)
p5.point(85, 20)
p5.point(85, 75)
p5.point(30, 75)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("2 points and 2 large purple points in middle-right of canvas")

p5.point(30, 20)
p5.point(85, 20)
p5.stroke("purple") # Change the color
p5.stroke_weight(10) # Make the points 10 pixels in size
p5.point(85, 75)
p5.point(30, 75)
```


## Syntax

`point(x, y, [z])`

## Parameters

`x: float` x-coordinate.

`y: float` y-coordinate.

`[z]: float` z-coordinate (for WebGL mode).
