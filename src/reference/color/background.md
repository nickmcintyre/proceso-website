# background

`background()`

## Description

The `background()` function sets the color used for the background of the p5 canvas.
The default background is transparent. This function is typically used within `draw()` to
clear the display window at the beginning of each frame, but it can be used inside `setup()`
to set the background on the first frame of animation or if the background need only be set once.

The color is either specified in terms of the RGB, HSB, or HSL color depending on the current `color_mode`.
(The default color space is RGB, with each value in the range from 0 to 255). The alpha range by default
is also 0 to 255.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Dark charcoal grey square")

# Grayscale integer value
p5.background(51)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Yellow square")

# R, G & B integer values
p5.background(255, 204, 0)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Royal blue square")

# H, S & B integer values
p5.color_mode(p5.HSB)
p5.background(255, 204, 100)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Red square")

# Named SVG/CSS color string
p5.background('red')
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Pink square")

# Three-digit hexadecimal RGB notation
p5.background("#fae")
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Dark gray square")

# Six-digit hexadecimal RGB notation
p5.background("#222222")
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Bright green square")

# Integer RGB notation
p5.background("rgb(0,255,0)")
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Soft green square")

# Integer RGBA notation
p5.background("rgba(0,255,0, 0.25)")
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Red square")

# Percentage RGB notation
p5.background("rgb(100%,0%,10%)")
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Light purple square")

# Percentage RGBA notation
p5.background("rgba(100%,0%,100%,0.5)")
```

## Syntax

`background(value, [v2], [v3], [v4])`

## Parameters

`value: str|int|list[int]` Color components, CSS color, or red or hue value (depending on the current color mode)

`[v2]: int` Green or saturation value (depending on the current color mode)

`[v3]: int` Blue or brightness value (depending on the current color mode)

`[v4]: int` Opacity of the background relative to current color range (default is 0-255)
