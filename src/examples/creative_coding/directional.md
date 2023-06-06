# Directional

Adapted from https://p5js.org/examples/lights-directional.html

Move the mouse to change the direction of the light. Directional light comes
from one direction and is stronger when hitting a surface squarely and weaker
if it hits at a a gentle angle. After hitting a surface, a directional light
scatters in all directions. 

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two gray spheres are illuminated when someone moves their mouse over them.")

radius = 200


def setup():
    p5.create_canvas(710, 400, p5.WEBGL)
    p5.no_stroke()
    p5.fill(200)


def draw():
    p5.no_stroke()
    p5.background(0)
    dir_y = (p5.mouse_y / p5.height - 0.5) * 4
    dir_x = (p5.mouse_x / p5.width - 0.5) * 4
    p5.directional_light(204, 204, 204, dir_x, dir_y, 1)
    p5.translate(-1.5 * radius, 0, 0)
    p5.sphere(radius)
    p5.translate(3 * radius, 0, 0)
    p5.sphere(radius)


p5.run_sketch(setup=setup, draw=draw)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/57568d94-91fb-47e7-b981-a21e877e447f/latest/" target="_blank">View sketch</a>
