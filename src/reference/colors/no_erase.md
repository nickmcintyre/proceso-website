# no_erase

`no_erase()`

## Description

Ends erasing that was started with `erase()`. The `fill()`, `stroke()`, and
`blend_mode()` settings will return to what they were prior to calling `erase()`.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Orange background, with two tall blue rectangles. A centered circle erased the first blue rectangle but not the second.")

p5.background(235, 145, 15)
p5.no_stroke()
p5.fill(30, 45, 220)
p5.rect(30, 10, 10, 80)
p5.erase()
p5.circle(50, 50, 60)
p5.no_erase()
p5.rect(70, 10, 10, 80)
```

## Syntax

`no_erase()`
