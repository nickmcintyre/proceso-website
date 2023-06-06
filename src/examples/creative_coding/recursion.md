# Recursion

Adapted from https://p5js.org/examples/structure-recursion.html

A demonstration of recursion, which means functions call themselves. A
recursive function must have a terminating condition, without which it will go
into an infinite loop. Notice how the `draw_circle()` function calls itself at
the end of its block. It continues to do this until the variable "level" is
equal to 1.

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A large circle is inscribed with smaller and smaller circles that shrink by half at each stage.")

p5.create_canvas(720, 560)
p5.no_stroke()


def draw_circle(x, radius, level):
    # 'level' is the variable that terminates the recursion once it reaches
    # a certain value (here, 1). If a terminating condition is not
    # specified, a recursive function keeps calling itself again and again
    # until it runs out of stack space - not a favourable outcome!
    tt = (126 * level) / 4.0
    p5.fill(tt)
    p5.circle(x, p5.height / 2, radius * 2)
    if level > 1:
        # 'level' decreases by 1 at every step and thus makes the terminating condition
        # attainable
        level = level - 1
        draw_circle(x - radius / 2, radius / 2, level)
        draw_circle(x + radius / 2, radius / 2, level)


draw_circle(p5.width / 2, 280, 6)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/7d81b89f-8f32-4e57-8a77-0d2a11d83e51/latest/" target="_blank">View sketch</a>
