# blue

`blue()`

## Description

Extracts the blue value from a color or pixel list.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two rectangles, light purple on left and royal blue on right.")

c = p5.color(175, 100, 220)
p5.fill(c)
p5.rect(15, 20, 35, 60) # Draw left rectangle
blue_value = p5.blue(c)
p5.fill(0, 0, blue_value)
p5.rect(50, 20, 35, 60) # Draw right rectangle
```

## Syntax

`blue(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Blue value
