# Iteration

Adapted from https://p5js.org/examples/control-iteration.html

Iteration with a "for" structure to construct repetitive forms. 

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Multiple sets of lines are drawn in grayscale on a dark gray background.")

num = 14

p5.create_canvas(720, 360)
p5.background(102)
p5.no_stroke()

# Draw white bars
p5.fill(255)
y = 60
for _ in range(int(num / 3)):
    p5.rect(50, y, 475, 10)
    y += 20

# Gray bars
p5.fill(51)
y = 40
for _ in range(num):
    p5.rect(405, y, 30, 10)
    y += 20

y = 50
for _ in range(num):
    p5.rect(425, y, 30, 10)
    y += 20

# Thin lines
y = 45
p5.fill(0)
for _ in range(num - 1):
    p5.rect(120, y, 40, 1)
    y += 20
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/ce44c49a-6039-420c-935a-5428fc9e4263/latest/" target="_blank">View sketch</a>
