# Video Capture

Adapted from https://p5js.org/examples/dom-video-capture.html

Capture video from the webcam and display on the canvas as well with invert
filter. Note that by default the capture feed shows up, too. You can hide the
feed by uncommenting the `capture.hide()` line. 

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A live video feed displayed with inverted colors.")

capture = None


def setup():
    p5.create_canvas(320, 240)
    global capture
    capture = p5.create_capture(p5.VIDEO)
    capture.size(320, 240)
    capture.hide()


def draw():
    p5.background(255)
    p5.image(capture, 0, 0, 320, 240)
    p5.apply_filter(p5.INVERT)


p5.run_sketch(setup=setup, draw=draw)
```

<a class="sd-sphinx-override sd-btn sd-text-wrap sd-btn-primary sd-rounded-pill float-left" href="https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/c284b2b1-2926-4e48-977e-cb545310bd67/latest/" target="_blank">View sketch</a>
