# square

`square()`

## Description

Draws a square to the screen. A square is a four-sided shape with every angle
at ninety degrees, and equal side size. This function is a special case of
the `rect()` function, where the width and height are the same, and the
parameter is called "s" for side size. By default, the first two parameters
set the location of the upper-left corner, the third sets the side size of the
square. The way these parameters are interpreted, may be changed with the
`rect_mode()` function.

The fourth, fifth, sixth and seventh parameters, if specified, determine
corner radius for the top-left, top-right, lower-right and lower-left
corners, respectively. An omitted corner radius parameter is set to the
value of the previously specified radius value in the parameter list.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with black outline in mid-right of canvas")

# Draw a square at location (30, 20) with a side size of 55.
p5.square(30, 20, 55)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "White square with black outline and round edges in mid-right of canvas"
)

# Draw a square with rounded corners, each having a radius of 20.
p5.square(30, 20, 55, 20)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "White square with black outline and round edges of different radii"
)

# Draw a square with rounded corners having the following radii:
# top-left = 20, top-right = 15, bottom-right = 10, bottom-left = 5.
p5.square(30, 20, 55, 20, 15, 10, 5)
```

## Syntax

`square(x, y, s, [tl], [tr], [br], [bl])`

## Parameters

`x: float` x-coordinate of the rectangle.

`y: float` y-coordinate of the rectangle.

`s: float` Side size of the rectangle.

`[tl]: float` Radius of top-left corner.

`[tr]: float` Radius of top-right corner.

`[br]: float` Radius of bottom-right corner.

`[bl]: float` Radius of bottom-left corner.
