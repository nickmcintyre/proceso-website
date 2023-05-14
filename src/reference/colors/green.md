# green

`green()`

## Description

Extracts the green value from a color or pixel list.

## Examples

```python
from proceso import Sketch


p5 = Sketch()
p5.describe("Blue rectangle on left and green on right, both with black outlines & 35×60.")

c = p5.color(20, 75, 200) # Define color 'c'
p5.fill(c) # Use color variable 'c' as fill color
p5.rect(15, 20, 35, 60) # Draw left rectangle

green_value = p5.green(c) # Get green in 'c'
print(green_value) # Print "75.0"
p5.fill(0, green_value, 0) # Use 'green_value' in new fill
p5.rect(50, 20, 35, 60) # Draw right rectangle
```

## Syntax

`green(color)`

## Parameters

`color: list[int]|str` Color components or CSS color

## Returns

`int` Green value
