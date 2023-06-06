# Continuous Lines

Adapted from https://p5js.org/examples/drawing-continuous-lines.html

Click and drag the mouse to draw a line. 

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A white line is drawn when someone presses down on a light blue background.")


def setup():
    p5.create_canvas(710, 400)
    p5.background("dodgerblue")


def draw():
    p5.stroke(255)
    if p5.is_mouse_pressed == True:
        p5.line(p5.mouse_x, p5.mouse_y, p5.pmouse_x, p5.pmouse_y)


def key_pressed():
    p5.background("dodgerblue")


p5.run_sketch(setup=setup, draw=draw, key_pressed=key_pressed)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/043632a3-6747-4f02-8d30-900f4b278199/latest/" target="_blank">View sketch</a>
