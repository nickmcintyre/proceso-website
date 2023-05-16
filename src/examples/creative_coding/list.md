# List

Adapted from https://p5js.org/examples/arrays-array.html

Each piece of data in a list is identified by an index number representing its
position in the list. Lists are zero based, which means that the first
element in the list is [0], the second element is [1], and so on. In this
example, a list named "coswave" is created and filled with the cosine
values. This data is displayed three separate ways on the screen. 

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Three rows of vertical lines whose stroke varies from black to white.")

p5.create_canvas(720, 360)
p5.background(255)

coswave = []

for i in range(p5.width):
    amount = p5.remap(i, 0, p5.width, 0, p5.PI)
    coswave.append(p5.abs(p5.cos(amount)))

y1 = 0
y2 = p5.height / 3
for i in range(0, p5.width, 3):
    p5.stroke(coswave[i] * 255)
    p5.line(i, y1, i, y2)

y1 = y2
y2 = y1 + y1
for i in range(0, p5.width, 3):
    p5.stroke((coswave[i] * 255) / 4)
    p5.line(i, y1, i, y2)

y1 = y2
y2 = p5.height
for i in range(0, p5.width, 3):
    p5.stroke(255 - coswave[i] * 255)
    p5.line(i, y1, i, y2)
```
