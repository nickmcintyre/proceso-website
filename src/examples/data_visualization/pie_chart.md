# Pie Chart

Adapted from https://p5js.org/examples/form-pie-chart.html

Uses the `arc()` function to generate a pie chart from the data stored in a list. 

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A grayscale pie chart on a dark gray background.")

angles = [30, 10, 45, 35, 60, 38, 75, 67]

p5.create_canvas(720, 400)
p5.background(100)
p5.no_stroke()


def pie_chart(diameter, data):
    last_angle = 0
    for i in range(len(data)):
        gray = p5.remap(i, 0, len(data), 0, 255)
        p5.fill(gray)
        p5.arc(
            p5.width / 2,
            p5.height / 2,
            diameter,
            diameter,
            last_angle,
            last_angle + p5.radians(angles[i]),
        )
        last_angle += p5.radians(angles[i])


pie_chart(300, angles)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/2916b26c-6a4a-47ea-9467-3b3c1bfb768f/latest/" target="_blank">View sketch</a>
