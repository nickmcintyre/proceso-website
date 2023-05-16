# hue

`hue()`

## Description

Extracts the hue value from a color or pixel list.

Hue exists in both HSB and HSL. This function will return the
HSB-normalized hue when supplied with an HSB color object (or when
supplied with a pixel list while the color mode is HSB),but will
default to the HSL-normalized hue otherwise.
(The values will only be different if the maximum hue setting for
each system is different.)

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two rectangles, salmon pink on left and black on right, both 35×60.")

p5.no_stroke()
p5.color_mode(p5.HSB, 255)
c = p5.color(0, 126, 255)
p5.fill(c)
p5.rect(15, 20, 35, 60)
value = p5.hue(c) # Sets 'value' to "0"
p5.fill(value)
p5.rect(50, 20, 35, 60)
```

## Syntax

`hue(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Hue value
