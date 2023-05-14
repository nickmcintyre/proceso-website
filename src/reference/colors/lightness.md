# lightness

`lightness()`

## Description

Extracts the HSL lightness value from a color or pixel list.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two rectangles, light pastel green on left and dark grey on right, both 35×60.")

p5.no_stroke()
p5.color_mode(p5.HSL)
c = p5.color(156, 100, 50, 1)
p5.fill(c)
p5.rect(15, 20, 35, 60)
value = p5.lightness(c) # Sets 'value' to 50
p5.fill(value)
p5.rect(50, 20, 35, 60)
```

## Syntax

`lightness(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Lightness value
