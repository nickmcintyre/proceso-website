# smooth

`smooth()`

## Description

Draws all geometry with smooth (anti-aliased) edges.
`smooth()` will also improve image quality of resized images.

Note that `smooth()` is active by default in 2D mode; `no_smooth()` can be
used to disable smoothing of geometry, images, and fonts.

In 3D mode, `no_smooth()` is enabled by default, so it is necessary to
call `smooth()` if you would like smooth (antialiased) edges on your
geometry.

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

`smooth()`
