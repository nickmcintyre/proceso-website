# alpha

`alpha()`

## Description

Extracts the alpha value from a color or pixel list.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Left half of canvas light blue and right half light charcoal grey.")

p5.no_stroke()
c = p5.color(0, 126, 255, 102)
p5.fill(c)
p5.rect(15, 15, 35, 70)
value = p5.alpha(c) # Sets 'value' to 102
p5.fill(value)
p5.rect(50, 15, 35, 70)
```

## Syntax

`alpha(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Alpha value
