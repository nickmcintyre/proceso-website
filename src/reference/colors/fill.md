# fill

`fill()`

## Description

Sets the color used to fill shapes. For example, if you run
`fill(204, 102, 0)`, all shapes drawn after the `fill()` command will be
filled with the color orange. This color is either specified in terms of the
RGB or HSB color depending on the current `color_mode()`. (The default color
space is RGB, with each value in the range from 0 to 255). The alpha range by
default is also 0 to 255.

If a single string argument is provided, RGB, RGBA and Hex CSS color
strings and all named color strings are supported. In this case, an
alpha number value as a second argument is not supported, the RGBA
form should be used.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Dark charcoal grey square with black outline in center of canvas")

# Grayscale integer value
p5.fill(51)
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Yellow square with black outline in center of canvas")

# R, G & B integer values
p5.fill(255, 204, 0)
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Royal blue square with black outline in center of canvas")

# H, S & B integer values
p5.color_mode(p5.HSB)
p5.fill(255, 204, 100)
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Red square with black outline in center of canvas")

# Named SVG/CSS color string
p5.fill("red")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Pink square with black outline in center of canvas")

# Three-digit hexadecimal RGB notation
p5.fill("#fae")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Black square with black outline in center of canvas")

# Six-digit hexadecimal RGB notation
p5.fill("#222222")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Bright green square with black outline in center of canvas")

# Integer RGB notation
p5.fill("rgb(0,255,0)")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Soft green square with black outline in center of canvas")

# Integer RGBA notation
p5.fill("rgba(0,255,0, 0.25)")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Red square with black outline in center of canvas")

# Percentage RGB notation
p5.fill("rgb(100%,0%,10%)")
p5.square(20, 20, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Dark fuchsia square with black outline in center of canvas")

# Percentage RGBA notation
p5.fill("rgba(100%,0%,100%,0.5)")
p5.square(20, 20, 60)
```

## Syntax

`fill(value, [v2], [v3], [v4])`

## Parameters

`value: str|int|list[int]` Color components, CSS color, or red or hue value (depending on the current color mode)

`[v2]: int` Green or saturation value (depending on the current color mode)

`[v3]: int` Blue or brightness value (depending on the current color mode)

`[v4]: int` Opacity of the background relative to current color range (default is 0-255)
