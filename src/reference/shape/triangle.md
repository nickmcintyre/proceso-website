# triangle

`triangle()`

## Description

Draws a triangle to the canvas. A triangle is a plane created by connecting
three points. The first two arguments specify the first point, the middle two
arguments specify the second point, and the last two arguments specify the
third point.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White triangle with black outline in mid-right of canvas")

p5.triangle(30, 75, 58, 20, 86, 75)
```

## Syntax

`triangle(x1, y1, x2, y2, x3, y3)`

## Parameters

`x1: float` x-coordinate of the first point.

`y1: float` y-coordinate of the first point.

`x2: float` x-coordinate of the second point.

`y2: float` y-coordinate of the second point.

`x3: float` x-coordinate of the third point.

`y3: float` y-coordinate of the third point.
