# Variables

Adapted from https://p5js.org/examples/data-variables.html

Variables are used for storing values. In this example, change the values of
variables to affect the composition. 

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Three sets of four gray, horizontal lines on a black background.")

p5.create_canvas(720, 400)
p5.background(0)
p5.stroke(153)
p5.stroke_weight(4)
p5.stroke_cap(p5.SQUARE)

a = 50
b = 120
c = 180

p5.line(a, b, a + c, b)
p5.line(a, b + 10, a + c, b + 10)
p5.line(a, b + 20, a + c, b + 20)
p5.line(a, b + 30, a + c, b + 30)

a = a + c
b = p5.height - b

p5.line(a, b, a + c, b)
p5.line(a, b + 10, a + c, b + 10)
p5.line(a, b + 20, a + c, b + 20)
p5.line(a, b + 30, a + c, b + 30)

a = a + c
b = p5.height - b

p5.line(a, b, a + c, b)
p5.line(a, b + 10, a + c, b + 10)
p5.line(a, b + 20, a + c, b + 20)
p5.line(a, b + 30, a + c, b + 30)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/84f48715-5d4a-460e-b585-9c7ee5ca26a8/latest/" target="_blank">View sketch</a>
