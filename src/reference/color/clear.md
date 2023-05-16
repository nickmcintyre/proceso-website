# clear

`clear()`

## Description

Clears the pixels within a buffer.
This function only clears the canvas. It will not clear objects
created by `create_x()` functions such as `create_video()` or
`create_div()`. Unlike the main graphics context, pixels in additional
graphics areas created with `create_graphics()` can be entirely or
partially transparent. This function clears everything to make all of
the pixels 100% transparent.

Note: In WebGL mode, this function can be passed normalized RGBA color
values in order to clear the screen to a specific color. In addition
to color, it will also clear the depth buffer. If you are not using
the WebGL renderer these color values will have no effect.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Small white circles are continually drawn at mouse’s x- and y-coordinates.")


# Clear the screen on mouse press.
def setup():
    p5.create_canvas(200, 200)
    p5.background(128)


def draw():
    p5.circle(p5.mouse_x, p5.mouse_y, 20)


def mouse_pressed():
    p5.clear()
    p5.background(128)


p5.run_sketch(draw=draw, mouse_pressed=mouse_pressed)
```

## Syntax

`clear([r], [g], [b], [a])`

## Parameters

`[r]: int` Normalized red value

`[g]: int` Normalized green value

`[b]: int` Normalized blue value

`[a]: int` Normalized alpha value
