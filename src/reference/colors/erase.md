# erase

`erase()`

## Description

All drawing that follows `erase()` will subtract from the canvas.
Erased areas will reveal the web page underneath the canvas. Erasing
can be canceled with `no_erase()`.

Drawing done with `image()` and `background()` in between `erase()` and
`no_erase()` will not erase the canvas but works as usual.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("60×60 centered pink square, purple background. Circular area in top-left of square is erased white.")

p5.background(100, 100, 250)
p5.fill(250, 100, 100)
p5.square(20, 20, 60)
p5.erase()
p5.square(25, 30)
p5.no_erase()
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("60×60 centered purple square, mint green background. Triangle in top-right is partially erased with fully erased outline.")

p5.background(150, 250, 150)
p5.fill(100, 100, 250)
p5.rect(20, 20, 60, 60)
p5.stroke_weight(5)
p5.erase(150, 255)
p5.triangle(50, 10, 70, 50, 90, 10)
p5.no_erase()
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("60×60 centered teal sphere, yellow background. Torus rotating around sphere erases to reveal black text underneath.")


def setup():
    p5.smooth()
    p5.create_canvas(100, 100, p5.WEBGL)
    # Make a <p> element and put it behind the canvas
    p = create_p("I am a dom element")
    p.center()
    p.style("font-size", "20px")
    p.style("text-align", "center")
    p.style("z-index", "-9999")


def draw():
    p5.background(250, 250, 150)
    p5.fill(15, 195, 185)
    p5.no_stroke()
    p5.sphere(30)
    p5.erase()
    p5.rotate_y(p5.frame_count * 0.02)
    p5.translate(0, 0, 40)
    p5.torus(15, 5)
    p5.no_erase()
  

p5.run_sketch(setup=setup, draw=draw)
```

## Syntax

`erase([strength_fill], [strength_stroke])`

## Parameters

`[strength_fill]: int` A number (0-255) for the strength of erasing for a shape's fill. This will default to 255 when no argument is given, which is full strength.

`[strength_stroke]: int` A number (0-255) for the strength of erasing for a shape's stroke. This will default to 255 when no argument is given, which is full strength.
