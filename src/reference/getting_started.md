# Getting Started

proceso sketches run in your web browser, so all you need is a text editor to get started. Here is an example of how to create a proceso sketch with PyScript:

**index.html**

```html
<!DOCTYPE html>
<html lang="en-us">

<head>
    <title>My Sketch</title>
    <meta charset="utf-8" />

    <link rel="stylesheet" href="https://pyscript.net/releases/2023.03.1/pyscript.css" />
    <script defer src="https://pyscript.net/releases/2023.03.1/pyscript.js"></script>
    <link rel="stylesheet" href="style.css" />
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.6.0/p5.min.js"></script>
    <py-config>
        packages = ["numpy", "proceso"]
    </py-config>
</head>

<body>
    <main></main>
    <py-script src="sketch.py"></py-script>
</body>

</html>
```

**style.css**

```css
html,
body {
    margin: 0;
    padding: 0;
}

canvas {
    display: block;
}
```

**sketch.py**

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A screen reader accessible description for the canvas.")
```

## Static Sketches

Similar to [Processing](https://processing.org), proceso enables beginners to start programming with "static sketches" before introducing animation and interaction. The following example draws a few shapes and a flower on the screen.

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A rectangle, circle, triangle, and flower drawn in pink on a gray background.")

# Create the canvas
p5.create_canvas(720, 400)
p5.background(200)

# Set colors
p5.fill(204, 101, 192, 127)
p5.stroke(127, 63, 120)

# A rectangle
p5.rect(40, 120, 120, 40)
# A circle
p5.circle(240, 240, 80)
# A triangle
p5.triangle(300, 100, 320, 100, 310, 80)

# A design for a simple flower
p5.translate(580, 200)
p5.no_stroke()
for _ in range(10):
    p5.ellipse(0, 30, 20, 80)
    p5.rotate(p5.PI / 5)
```

## Active Sketches

proceso's "active sketches" provide the `run_sketch()` method to handle initialization, looping, and events. The sketch below simulates the synchronization behavior observed in some species of fireflies.

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Ten white circles moving like fireflies on a dark blue background.")

bugs = []
num_bugs = 10
coupling: object
KN: float


def setup():
    p5.create_canvas(720, 400)
    global coupling
    coupling = p5.create_slider(0, 10, 5)
    for _ in range(num_bugs):
        bugs.append(Bug())


def draw():
    p5.background("midnightblue")

    global KN
    KN = coupling.value() / num_bugs

    for bug in bugs:
        bug.sync()

    for bug in bugs:
        bug.draw()
        bug.update()
        bug.check_edges()


class Bug:
    def __init__(self):
        self.x = p5.width * 0.5
        self.y = p5.height * 0.5
        self.r = 5
        self.angle = p5.random(p5.TWO_PI)
        self.da_dt = 1
        self.dt = 0.01
        self.freq = p5.random(5, 10)

    def draw(self):
        a = p5.remap(self.angle % p5.TWO_PI, 0, p5.TWO_PI, 0, 255)
        p5.fill(255, a)
        p5.stroke(255, a)
        p5.circle(self.x, self.y, 2 * self.r)

    def update(self):
        self.x += p5.cos(self.angle)
        self.y += p5.sin(self.angle)
        self.angle += self.da_dt * self.dt

    def check_edges(self):
        if self.x > p5.width + self.r:
            self.x = -self.r
        if self.x < -self.r:
            self.x = p5.width + self.r
        if self.y > p5.height + self.r:
            self.y = -self.r
        if self.y < -self.r:
            self.y = p5.height + self.r

    def sync(self):
        self.da_dt = self.freq
        for bug in bugs:
            self.da_dt += KN * p5.sin(bug.angle - self.angle)


p5.run_sketch(setup=setup, draw=draw)
```

## Coding Environment

**Cloud (account required): PyScript**

[PyScript](https://pyscript.com) is a great way to run proceso sketches with PyScript. Here is a [project template](https://4b2d42a1-0e0c-430f-8b20-4b2c7ff0dc3e.pyscriptapps.com/58197361-1c5f-4d47-93a9-91570255fe85/latest/).

**Cloud (no account required): JupyterLite**

Coming soonish.

**Local: Anaconda + VS Code**

Here is one possible setup for running sketches on your local machine:

1. Install the [Anaconda Distribution of Python](https://www.anaconda.com/download).
2. Install [Visual Studio Code](https://code.visualstudio.com/).
3. [Get started with Anaconda Navigator](https://docs.anaconda.com/free/navigator/) and create a new Python environment with Python 3.10.
4. Use the Navigator to open a terminal with your new Python environment and `pip install proceso`.
5. Open VS Code and install the [Microsoft Python extension](https://code.visualstudio.com/docs/languages/python) to enable helpful features such as documentation, autocompletion, and so on.
6. [Select the interpreter](https://code.visualstudio.com/docs/python/environments#_manually-specify-an-interpreter) created by your new Python environment.
7. Add your HTML, CSS, and Python files and start coding.
8. [Open the terminal](https://code.visualstudio.com/docs/terminal/basics) in VS Code and run `python -m http.server` to view your sketch in the browser.