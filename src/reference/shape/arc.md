# arc

`arc()`

## Description

Draw an arc to the screen. If called with only `x`, `y`, `w`, `h`, `start` and
`stop`, the arc will be drawn and filled as an open pie segment. If a mode
parameter is provided, the arc will be filled like an open semi-circle
(`OPEN`), a closed semi-circle (`CHORD`), or as a closed pie segment (`PIE`).
The origin may be changed with the `ellipse_mode()` function.

The arc is always drawn clockwise from wherever start falls to wherever
stop falls on the ellipse. Adding or subtracting `TWO_PI` to either angle
does not change where they fall. If both start and stop fall at the same
place, a full ellipse will be drawn. Be aware that the y-axis increases in
the downward direction, therefore angles are measured clockwise from the
positive x-direction ("3 o'clock").

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "Shattered outline of ellipse with a quarter of a white circle bottom-right"
)

p5.arc(50, 55, 50, 50, 0, p5.HALF_PI)
p5.no_fill()
p5.arc(50, 55, 60, 60, p5.HALF_PI, p5.PI)
p5.arc(50, 55, 70, 70, p5.PI, p5.PI + p5.QUARTER_PI)
p5.arc(50, 55, 80, 80, p5.PI + p5.QUARTER_PI, p5.TWO_PI)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White ellipse with top right quarter missing")

p5.arc(50, 50, 80, 80, 0, p5.PI + p5.QUARTER_PI)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White ellipse with black outline with top right missing")

p5.arc(50, 50, 80, 80, 0, p5.PI + p5.QUARTER_PI, p5.OPEN)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White open arc with black outline with top right missing")

p5.arc(50, 50, 80, 80, 0, p5.PI + p5.QUARTER_PI, p5.CHORD)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "White ellipse with top right quarter missing with black outline around the shape"
)

p5.arc(50, 50, 80, 80, 0, p5.PI + p5.QUARTER_PI, p5.PIE)
```

## Syntax

`arc(x, y, w, h, start, stop, [mode], [detail])`

## Parameters

`x: float` x-coordinate of the arc's ellipse.

`y: float` y-coordinate of the arc's ellipse.

`w: float` Width of the arc's ellipse by default.

`h: float` Height of the arc's ellipse by default.

`start: float` Angle to start the arc, specified in radians.

`stop: float` Angle to stop the arc, specified in radians.

`[mode]: str` Optional parameter to determine the way of drawing the arc. Either CHORD, PIE or OPEN.

`[detail]: int` Optional parameter for WebGL mode only. This is to specify the number of vertices that makes up the perimeter of the arc. Default value is 25. Won't draw a stroke for a detail of more than 50.
