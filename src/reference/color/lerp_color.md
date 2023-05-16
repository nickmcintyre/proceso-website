# lerp_color

`lerp_color()`

## Description

Blends two colors to find a third color somewhere between them. The `amt`
parameter is the amount to interpolate between the two values where 0.0
is equal to the first color, 0.1 is very near the first color, 0.5 is
halfway in between, etc. An amount below 0 will be treated as 0. Likewise,
amounts above 1 will be capped at 1. This is different from the behavior
of `lerp()`, but necessary because otherwise numbers outside the range
will produce strange and unexpected colors.

The way that colors are interpolated depends on the current color mode.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Four rectangles one tan, brown, brownish purple, purple, with white outlines & 20×60")

p5.color_mode(p5.RGB)
p5.stroke(255)
p5.background(51)
start = p5.color(218, 165, 32)
end = p5.color(72, 61, 139)
p5.color_mode(p5.RGB) # Try changing to HSB.
inter_a = p5.lerp_color(start, end, 0.33)
inter_b = p5.lerp_color(start, end, 0.66)
p5.fill(start)
p5.rect(10, 20, 20, 60)
p5.fill(inter_a)
p5.rect(30, 20, 20, 60)
p5.fill(inter_b)
p5.rect(50, 20, 20, 60)
p5.fill(end)
p5.rect(70, 20, 20, 60)
```

## Syntax

`lerp_color(c1, c2, amt)`

## Parameters

`c1: str | list[int]` Interpolate from this color

`c2: str | list[int]` Interpolate to this color

`amt: float` Number between 0 and 1

## Returns

`str` Interpolated color as a RGBA color string
