# color

`color()`

## Description

Creates colors for storing in variables of the color datatype.
The parameters are interpreted as RGB or HSB values depending on the
current `color_mode()`. The default mode is RGB values from 0 to 255 and,
therefore, the function call `color(255, 204, 0)` will return a bright
yellow color.

Note that if only one value is provided to `color()`, it will be interpreted
as a grayscale value. Add a second value, and it will be used for alpha
transparency. When three values are specified, they are interpreted as
either RGB or HSB values. Adding a fourth value applies alpha
transparency.

If a single string argument is provided, RGB, RGBA and Hex CSS color
strings and all named color strings are supported. In this case, an alpha
number value as a second argument is not supported, the RGBA form should
be used.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Yellow rect in middle right of canvas, with 55 pixel width and height.")

c = p5.color(255, 204, 0)
p5.fill(c)
p5.no_stroke()
p5.rect(30, 20, 55, 55)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Yellow ellipse in top left of canvas, black ellipse in bottom right, both 80×80.")

c = p5.color(255, 204, 0)
p5.fill(c)
p5.no_stroke()
p5.circle(25, 25, 80) # Draw left circle
# Using only one value generates a grayscale value.
c = p5.color(65)
p5.fill(c)
p5.circle(75, 75, 80)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Bright fuchsia rectangle in middle of canvas, 60 pixel width and height.")

# You can use named SVG & CSS colors
c = p5.color('magenta')
p5.fill(c)
p5.no_stroke()
p5.rect(20, 20, 60, 60)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two bright green rectangles on opposite sides of the canvas, both 45×80.")

# Example of hex color codes
p5.no_stroke()
c = p5.color("#0f0")
p5.fill(c)
p5.rect(0, 10, 45, 80)
c = p5.color("#00ff00")
p5.fill(c)
p5.rect(55, 10, 45, 80)
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Four blue rectangles in each corner of the canvas, each are 35×35.")

# RGB and RGBA color strings are also supported
# these all set to the same color (solid blue)
p5.no_stroke()
c = p5.color("rgb(0,0,255)")
p5.fill(c)
p5.rect(10, 10, 35, 35) # Draw rectangle
c = p5.color("rgb(0%, 0%, 100%)")
p5.fill(c)
p5.rect(55, 10, 35, 35) # Draw rectangle
c = p5.color("rgba(0, 0, 255, 1)")
p5.fill(c)
p5.rect(10, 55, 35, 35) # Draw rectangle
c = p5.color("rgba(0%, 0%, 100%, 1)")
p5.fill(c)
p5.rect(55, 55, 35, 35) # Draw rectangle
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Bright sea green rectangle on left and darker rectangle on right of canvas, both 45×80.")

# HSL color can also be specified by value
c = p5.color("hsl(160, 100%, 50%)")
p5.no_stroke()
p5.fill(c)
p5.rect(0, 10, 45, 80) # Draw rectangle
c = p5.color("hsla(160, 100%, 50%, 0.5)")
p5.fill(c)
p5.rect(55, 10, 45, 80) # Draw rectangle
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Dark green rectangle on left and lighter green rectangle on right of canvas, both 45×80.")

# HSB color can also be specified
c = p5.color("hsb(160, 100%, 50%)")
p5.no_stroke()
p5.fill(c)
p5.rect(0, 10, 45, 80) # Draw rectangle
c = p5.color("hsba(160, 100%, 50%, 0.5)")
p5.fill(c)
p5.rect(55, 10, 45, 80) # Draw rectangle
```

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Dark blue rectangle on left and light teal rectangle on right of canvas, both 45×80.")

p5.no_stroke()
c = p5.color(50, 55, 100)
p5.fill(c)
p5.rect(0, 10, 45, 80) # Draw left rect
p5.color_mode(p5.HSB, 100)
c = p5.color(50, 55, 100)
p5.fill(c)
p5.rect(55, 10, 45, 80)
```

## Syntax

`color(value, [v2], [v3], [v4])`

## Parameters

`value: str|int|list[int]` Color components, CSS color, or red or hue value (depending on the current color mode)

`[v2]: int` Green or saturation value (depending on the current color mode)

`[v3]: int` Blue or brightness value (depending on the current color mode)

`[v4]: int` Opacity of the background relative to current color range (default is 0-255)

## Returns

`str` Color as a RGBA color string
