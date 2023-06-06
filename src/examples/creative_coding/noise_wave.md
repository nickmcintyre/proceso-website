# Noise Wave

Adapted from https://p5js.org/examples/math-noise-wave.html

Using Perlin Noise to generate a wave-like pattern. Original by Daniel Shiffman.

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A noisy, white wave drawn on a dark gray background.")

yoff = 0.0  # 2nd dimension of perlin noise


def setup():
    p5.create_canvas(710, 400)


def draw():
    global yoff

    p5.background(51)

    p5.fill(255)
    # We are going to draw a polygon out of the wave points
    p5.begin_shape()

    xoff = 0  # Option #1: 2D Noise
    # xoff = yoff # Option #2: 1D Noise

    # Iterate over horizontal pixels
    for x in range(0, p5.width + 10, 10):
        # Calculate a y value according to noise, map to

        # Option #1: 2D Noise
        y = p5.remap(p5.noise(xoff, yoff), 0, 1, 200, 300)

        # Option #2: 1D Noise
        # y = p5.remap(p5.noise(xoff), 0, 1, 200,300)

        # Set the vertex
        p5.vertex(x, y)
        # Increment x dimension for noise
        xoff += 0.05
    # increment y dimension for noise
    yoff += 0.01
    p5.vertex(p5.width, p5.height)
    p5.vertex(0, p5.height)
    p5.end_shape(p5.CLOSE)


p5.run_sketch(setup=setup, draw=draw)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/4ba9a8cd-33d7-4c91-909f-2a1265d5991e/latest/" target="_blank">View sketch</a>
