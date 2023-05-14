# brightness

`brightness()`

## Description

Extracts the HSB brightness value from a color or pixel list.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Left half of canvas salmon pink and the right half with its brightness colored white.")

p5.no_stroke()
p5.color_mode(p5.HSB, 255)
c = p5.color(0, 126, 255)
p5.fill(c)
p5.rect(15, 20, 35, 60)
value = p5.brightness(c) # Sets 'value' to 255
p5.fill(value)
p5.rect(50, 20, 35, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Left half of canvas olive colored and the right half with its brightness color gray.")

p5.no_stroke()
p5.color_mode(p5.HSB, 255)
c = p5.color('hsb(60, 100%, 50%)')
p5.fill(c)
p5.rect(15, 20, 35, 60)
value = p5.brightness(c) # A 'value' of 50% is 127.5
p5.fill(value)
p5.rect(50, 20, 35, 60)
```

## Syntax

`brightness(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Brightness value
