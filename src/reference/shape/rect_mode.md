# rect_mode

`rect_mode()`

## Description

Modifies the location from which rectangles are drawn by changing the
way in which parameters given to `rect()` are interpreted.

The default mode is CORNER, which interprets the first two parameters as
the upper-left corner of the shape, while the third and fourth parameters
are its width and height.

`rect_mode(CORNERS)` interprets the first two parameters as the location of
one of the corners, and the third and fourth parameters as the location
of the diagonally opposite corner. Note, the rectangle is drawn between
the coordinates, so it is not necessary that the first corner be the
upper left corner.

`rect_mode(CENTER)` interprets the first two parameters as the shape's center
point, while the third and fourth parameters are its width and height.

`rect_mode(RADIUS)` also uses the first two parameters as the shape's center
point, but uses the third and fourth parameters to specify half of the
shape's width and height respectively.

The parameter to this function must be written in ALL CAPS because they
are predefined as constants in ALL CAPS and Python is a case-sensitive
language.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "A dark gray square drawn at the top-left corner of a white square"
)

p5.rect_mode(p5.CORNER)
p5.fill(255)
p5.rect(25, 25, 50, 50) # Draw white rectangle using CORNER mode

p5.rect_mode(p5.CORNERS)
p5.fill(100)
p5.rect(25, 25, 50, 50) # Draw gray rectangle using CORNERS mode
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A dark gray square drawn at the center of a white square")

p5.rect_mode(p5.RADIUS)
p5.fill(255)
p5.rect(50, 50, 30, 30) # Draw white rectangle using RADIUS mode

p5.rect_mode(p5.CENTER)
p5.fill(100)
p5.rect(50, 50, 30, 30) # Draw gray rectangle using CENTER mode
```

## Syntax

`rect_mode(mode)`

## Parameters

`mode: str` Either CORNER, CORNERS, CENTER, or RADIUS.
