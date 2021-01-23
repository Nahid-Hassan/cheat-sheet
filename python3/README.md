# Python Cheat Sheet

This `README.md` file contains Python3 all topics tips and tricks

## Table of Contents

- [Python Cheat Sheet](#python-cheat-sheet)
  - [Table of Contents](#table-of-contents)
    - [Python - Function](#python---function)
    - [Python - Dunder Method](#python---dunder-method)

### Python - Function

```py
1. callable(object) # return true if function is callable else  return false.
2. func_object.__name__ # return the original function name.

def yell(text):
    return text.title()

bark = yell
bark.__name__ # return yell
bark.__qualname__ # return yell
```

### Python - Dunder Method

```py
1. __init__() # Initialize the object

class Adder:
    def __init__(self, x, y):
        self.x = x
        self.y = y

2. __call__() # Make object callable

class Adder:
    # ...
    def __call__(self, n):
        return self.x + self.y + n
Adder(10, 20)(30) # return 60
callable(Adder(29, 23)) # return True
```
