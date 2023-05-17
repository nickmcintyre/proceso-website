# stroke_cap

`stroke_cap()`

## Description

Sets the style for rendering line endings.
These ends are either rounded, squared, or extended, each of which
specified with the corresponding parameters: ROUND, SQUARE, or PROJECT.
The default cap is ROUND.

The parameter to this function must be written in ALL CAPS because they
are predefined as constants in ALL CAPS and Python is a case-sensitive
language.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe(
    "Three black, horizontal lines. The top line has rounded edges" +
    " and the bottom two lines have square edges."
)

# Example of different stroke_caps
p5.stroke_weight(12.0)
p5.stroke_cap(p5.ROUND)
p5.line(20, 30, 80, 30)
p5.stroke_cap(p5.SQUARE)
p5.line(20, 50, 80, 50)
p5.stroke_cap(p5.PROJECT)
p5.line(20, 70, 80, 70)
```

## Syntax

`stroke_cap(cap)`

## Parameters

`cap: str` Either ROUND, SQUARE, or PROJECT.
