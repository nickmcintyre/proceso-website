# red

`red()`

## Description

Extracts the red value from a color or pixel list.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Two rectangles, yellow on left and red on right, both with black outlines and 35×60.")

c = p5.color(255, 204, 0) # Define color 'c'
p5.fill(c) # Use color variable 'c' as fill color
p5.rect(15, 20, 35, 60) # Draw left rectangle

red_value = p5.red(c) # Get red in 'c'
print(red_value) # Print "255.0"
p5.fill(red_value, 0, 0) # Use 'red_value' in new fill
p5.rect(50, 20, 35, 60) # Draw right rectangle
```

## Syntax

`red(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Red value
