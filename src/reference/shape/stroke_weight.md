# stroke_weight

`stroke_weight()`

## Description

Sets the width of the stroke used for lines, points, and the border
around shapes.
All widths are set in units of pixels.

Note that it is affected by any transformation or scaling that has been
applied previously.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "Three black horizontal lines. The top line is the thinnest and the bottom line is the thickest"
)

# Example of different stroke weights
p5.stroke_weight(1) # Default
p5.line(20, 20, 80, 20)
p5.stroke_weight(4) # Thicker
p5.line(20, 40, 80, 40)
p5.stroke_weight(10) # Beastly
p5.line(20, 70, 80, 70)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two black horiztonal lines. The top line is thinner than the bottom line.")

# Example of stroke weights
# after transformations
p5.stroke_weight(1) # Default
p5.line(20, 20, 80, 20)
p5.scale(5) # Adding scale transformation
p5.stroke_weight(1) # Resulting strokeweight is 5
p5.line(4, 8, 16, 8) # Coordinates adjusted for scaling
```

## Syntax

`stroke_weight(weight)`

## Parameters

`weight: float` The weight of the stroke (in pixels).
