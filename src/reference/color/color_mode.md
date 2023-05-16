# color_mode

`color_mode()`

## Description

`color_mode()` changes the way p5 interprets color data. By default,
the parameters for `fill()`, `stroke()`, `background()`, and `color()` are
defined by values between 0 and 255 using the RGB color model.
This is equivalent to setting `color_mode(RGB, 255)`. Setting
`color_mode(HSB)` lets you use the HSB system instead. By default,
this is `color_mode(HSB, 360, 100, 100, 1)`. You can also use HSL.

Note: existing color objects remember the mode that they were created
in, so you can change modes as you like without affecting their
appearance.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Green to red gradient from bottom left to top right with shading from top left")

p5.no_stroke()
p5.color_mode(p5.RGB, 100)
for i in range(100):
    for j in range(100):
        p5.stroke(i, j, 0)
        p5.point(i, j)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Rainbow gradient from left to right. Brightness increasing to white at top.")

p5.no_stroke()
p5.color_mode(p5.HSB, 100)
for i in range(100):
    for j in range(100):
        p5.stroke(i, j, 0)
        p5.point(i, j)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("value of color red 0.4980... written on canvas")

p5.color_mode(RGB, 255)
c = p5.color(127, 255, 0)
p5.color_mode(p5.RGB, 1)
my_color = p5.red(c)
p5.text(my_color, 10, 10, 80, 80)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two translucent pink ellipse outlines at middle-left and at center")

p5.no_fill()
p5.color_mode(p5.RGB, 255, 255, 255, 1)
p5.background(255)
p5.stroke_weight(4)
p5.stroke(255, 0, 10, 0.3)
p5.ellipse(40, 40, 50, 50)
p5.ellipse(50, 50, 40, 40)
```

## Syntax

`color_mode(mode, [max1], [max2], [max3], [max4])`

## Parameters

`mode: str`  Either RGB, HSB or HSL, corresponding to Red/Green/Blue and Hue/Saturation/Brightness (or Lightness) 

`[max1]: int` Range for all values, or range for the red or hue depending on the current color mode

`[max2]: int` Range for the green or saturation depending on the current color mode

`[max3]: int` Range for the blue or brightness/lightness depending on the current color mode

`[max4]: int` Range for the alpha
