# stroke_join

`stroke_join()`

## Description

Sets the style of the joints which connect line segments.
These joints are either mitered, beveled, or rounded and specified with
the corresponding parameters: MITER, BEVEL, or ROUND. The default joint is
MITER in 2D mode and ROUND in WebGL mode.

The parameter to this function must be written in ALL CAPS because they
are predefined as constants in ALL CAPS and Python is a case-sensitive
language.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A black arrow with a pointed joint")

# Example of MITER type of joints
p5.no_fill()
p5.stroke_weight(10)
p5.stroke_join(p5.MITER)
p5.begin_shape()
p5.vertex(35, 20)
p5.vertex(65, 50)
p5.vertex(35, 80)
p5.end_shape()
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A black arrow with a flat joint")

# Example of BEVEL type of joints
p5.no_fill()
p5.stroke_weight(10)
p5.stroke_join(p5.BEVEL)
p5.begin_shape()
p5.vertex(35, 20)
p5.vertex(65, 50)
p5.vertex(35, 80)
p5.end_shape()
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("A black arrow with a rounded joint")

# Example of ROUND type of joints
p5.no_fill()
p5.stroke_weight(10)
p5.stroke_join(p5.ROUND)
p5.begin_shape()
p5.vertex(35, 20)
p5.vertex(65, 50)
p5.vertex(35, 80)
p5.end_shape()
```

## Syntax

`stroke_join(join)`

## Parameters

`join: str` Either MITER, BEVEL, or ROUND.
