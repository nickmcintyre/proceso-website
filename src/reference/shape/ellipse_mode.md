# ellipse_mode

`ellipse_mode()`

## Description

Modifies the location from which ellipses are drawn by changing the way
in which parameters given to `ellipse()`, `circle()` and `arc()` are
interpreted.

The default mode is CENTER, in which the first two parameters are
interpreted as the shape's center point's x- and y-coordinates
respectively, while the third and fourth parameters are its width and
height.

`ellipse_mode(RADIUS)` also uses the first two parameters as the shape's
center point's x and y coordinates, but uses the third and fourth
parameters to specify half of the shapes's width and height.

`ellipse_mode(CORNER)` interprets the first two parameters as the upper-left
corner of the shape, while the third and fourth parameters are its width
and height.

`ellipse_mode(CORNERS)` interprets the first two parameters as the location
of one corner of the ellipse's bounding box, and the third and fourth
parameters as the location of the opposite corner.

The parameter to this function must be written in ALL CAPS because they
are predefined as constants in ALL CAPS and Python is a case-sensitive
language.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A dark gray circle drawn inside a larger white circle, both with black outlines")

# Example showing RADIUS and CENTER ellipsemode with 2 overlaying ellipses
p5.ellipse_mode(p5.RADIUS)
p5.fill(255)
p5.ellipse(50, 50, 30, 30) # Outer white ellipse
p5.ellipse_mode(p5.CENTER)
p5.fill(100)
p5.ellipse(50, 50, 30, 30) # Inner gray ellipse
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "A dark gray circle drawn at the top-left of a larger white circle, both with black outlines"
)

# Example showing CORNER and CORNERS ellipseMode with 2 overlaying ellipses
p5.ellipse_mode(p5.CORNER)
p5.fill(255)
p5.ellipse(25, 25, 50, 50) # Outer white ellipse
p5.ellipse_mode(p5.CORNERS)
p5.fill(100)
p5.ellipse(25, 25, 50, 50) # Inner gray ellipse
```

## Syntax

`ellipse_mode(mode)`

## Parameters

`mode: str` Either CENTER, RADIUS, CORNER, or CORNERS.
