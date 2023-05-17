# no_smooth

`no_smooth()`

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
p5.describe("Two white circles aligned horizontally on a black background")

p5.background(0)
p5.no_stroke()
p5.smooth()
p5.ellipse(30, 48, 36, 36)
p5.no_smooth()
p5.ellipse(70, 48, 36, 36)
```

## Syntax

`no_smooth()`
