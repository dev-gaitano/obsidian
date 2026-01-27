---
id: Decorator
aliases:
  - Decorators
  - decorator
  - decorators
tags:
  - programming
  - python
status: adult
---
---

11:36, Tue 04 November 2025

---

A decorator is a [[Python programming language|python]] function that is used to enhance the behaviour of 
another [[Function|function]] or class definition, without modifiying the base function or
class.

The base function is passed in as an argument to the decorator. For example,

```python
@add_sprinkles
def get_ice_cream() -> None:
    print("Got Ice Cream")
```

is equivalent to.

```python
def get_ice_cream() -> None:
    print("Got Ice Cream")

get_ice_cream = add_sprinkles(get_ice_cream)
```

### See also:

[Wikipedia | Decorators](https://en.wikipedia.org/wiki/Python_syntax_and_semantics#Decorators)

