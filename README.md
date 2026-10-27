# Polygon Area Calculator

A Python project that uses object-oriented programming to model rectangles and squares. `Square` is a subclass of `Rectangle`, so it inherits all of its methods and keeps its sides equal.

## Features

- **Rectangle**: set width and height, and get the area, perimeter and diagonal
- **Square**: a subclass of `Rectangle` with `set_side`, where changing any dimension keeps both sides equal
- **Picture output**: `get_picture()` draws the shape using `*` characters, or returns `"Too big for picture."` if a side is over 50
- **Shape fitting**: `get_amount_inside(shape)` returns how many times another shape fits inside, with no rotation
- **Readable output**: `Rectangle(width=10, height=5)` and `Square(side=9)`

## Tech Stack

- Python 3, with no external dependencies

## Example

```python
from shape_calculator import Rectangle, Square

rect = Rectangle(10, 5)
print(rect.get_area())       # 50
print(rect.get_perimeter())  # 30
print(rect.get_diagonal())   # 11.180339887498949
print(rect)                  # Rectangle(width=10, height=5)
print(rect.get_picture())    # 5 rows of 10 asterisks

sq = Square(9)
print(sq)                    # Square(side=9)
sq.set_width(4)
print(sq)                    # Square(side=4)

big = Rectangle(15, 10)
print(big.get_amount_inside(Square(5)))  # 6
```

## What I Learned

- Using inheritance so a subclass reuses a parent class
- Overriding methods to keep a class's own rules, such as a square's equal sides
- Using `super()` and `__str__` for clean, readable objects
- Handling edge cases, such as shapes too big to draw

## Author

**Anupama**: [GitHub](https://github.com/talarianupama)