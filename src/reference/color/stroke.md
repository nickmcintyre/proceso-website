# stroke

`stroke()`

## Description

Sets the color used to draw lines and borders around shapes.
This color is either specified in terms of the RGB or HSB color
depending on the current `color_mode()` (the default color space is RGB,
with each value in the range from 0 to 255). The alpha range by
default is also 0 to 255.

If a single string argument is provided, RGB, RGBA and Hex CSS color
strings and all named color strings are supported. In this case, an
alpha number value as a second argument is not supported, the RGBA
form should be used.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with dark charcoal grey outline")

# Grayscale integer value
p5.stroke_weight(4)
p5.stroke(51)
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with yellow outline")

# R, G & B integer values
p5.stroke_weight(4)
p5.stroke(255, 204, 0)
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with royal blue outline")

# H, S & B integer values
p5.color_mode(p5.HSB)
p5.stroke_weight(4)
p5.stroke(255, 204, 100)
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with red outline")

# Named SVG/CSS color string
p5.stroke_weight(4)
p5.stroke("red")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with pink outline")

# Three-digit hexadecimal RGB notation
p5.stroke_weight(4)
p5.stroke("#fae")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with black outline")

# Six-digit hexadecimal RGB notation
p5.stroke_weight(4)
p5.stroke("#222222")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with bright green outline")

# Integer RGB notation
p5.stroke_weight(4)
p5.stroke("rgb(0,255,0)")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with soft green outline")

# Integer RGBA notation
p5.stroke_weight(4)
p5.stroke("rgba(0,255,0, 0.25)")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with red outline")

# Percentage RGB notation
p5.stroke_weight(4)
p5.stroke("rgb(100%,0%,10%)")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("White square with dark fuchsia outline")

# Percentage RGBA notation
p5.stroke_weight(4)
p5.stroke("rgba(100%,0%,100%,0.5)")
p5.square(20, 20, 60)
```

## Syntax

`stroke(value, [v2], [v3], [v4])`

## Parameters

`value: str|int|list[int]` Color components, CSS color, or red or hue value (depending on the current color mode)

`[v2]: int` Green or saturation value (depending on the current color mode)

`[v3]: int` Blue or brightness value (depending on the current color mode)

`[v4]: int` Opacity of the background relative to current color range (default is 0-255)
