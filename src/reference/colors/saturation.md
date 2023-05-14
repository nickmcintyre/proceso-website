# saturation

`saturation()`

## Description

Extracts the saturation value from a color or pixel list.

Saturation is scaled differently in HSB and HSL. This function will return the
HSB saturation when supplied with an HSB color object (or when supplied with a
pixel list while the color mode is HSB), but will default to the HSL
saturation otherwise.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two rectangles, deep pink on left and grey on right, both 35×60.")

p5.no_stroke()
p5.color_mode(p5.HSB, 255)
c = p5.color(0, 126, 255)
p5.fill(c)
p5.rect(15, 20, 35, 60)
value = p5.saturation(c) # Sets 'value' to 126
p5.fill(value)
p5.rect(50, 20, 35, 60)
```

## Syntax

`saturation(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Saturation value
