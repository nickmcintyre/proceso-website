# no_fill

`no_fill()`

## Description

Disables filling geometry. If both `no_stroke()` and `no_fill()` are called,
nothing will be drawn to the screen.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square at top-middle and empty square at center, both with black outlines.")

p5.square(15, 10, 55)
p5.no_fill()
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Black canvas with purple cube wireframe spinning.")


def setup():
    p5.create_canvas(100, 100, p5.WEBGL)


def draw():
    p5.background(0)
    p5.no_fill()
    p5.stroke(100, 100, 240)
    p5.rotate_x(p5.frame_count * 0.01)
    p5.rotate_y(p5.frame_count * 0.01)
    p5.box(45, 45, 45)


p5.run_sketch(setup=setup, draw=draw)
```

## Syntax

`no_fill()`
