# no_stroke

`no_stroke()`

## Description

Disables drawing the stroke (outline). If both `no_stroke()` and `no_fill()`
are called, nothing will be drawn to the screen.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square at center with no outline.")

p5.no_stroke()
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Black canvas with pink cube spinning")


def setup():
    p5.create_canvas(100, 100, p5.WEBGL)


def draw():
    p5.background(0)
    p5.no_stroke()
    p5.fill(240, 150, 150)
    p5.rotate_x(p5.frame_count * 0.01)
    p5.rotate_y(p5.frame_count * 0.01)
    p5.box(45, 45, 45)


p5.run_sketch(setup=setup, draw=draw)
```

## Syntax

`no_stroke()`
