# Creative Coding

proceso makes it easy to create visual, interactive computer programs that run in your web browser. The examples in this section demonstrate some of the package's capabilities, from drawing in 2D and 3D to utilizing your computer's webcam.

Here is a quick sketch of a circle moving along a <a href="https://en.wikipedia.org/wiki/Lissajous_curve" target="_blank">Lissajous curve</a>:

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "A purple circle moving in a figure eight on a light blue background."
)


def setup():
    p5.create_canvas(400, 400)
    p5.background("dodgerblue")


def draw():
    p5.translate(p5.width * 0.5, p5.height * 0.5)
    x = 80 * p5.cos(0.1 * p5.frame_count)
    y = 40 * p5.sin(0.2 * p5.frame_count)
    p5.stroke("white")
    p5.fill("orchid")
    p5.circle(x, y, 20)
    if p5.is_mouse_pressed:
        p5.background("dodgerblue")


p5.run_sketch(setup=setup, draw=draw)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/58197361-1c5f-4d47-93a9-91570255fe85/latest/" target="_blank">View sketch</a>
