---
id: Decorator
aliases:
  - Decorators
  - decorator
  - decorators
tags:
  - programming
  - python
status: child
---
---

11:36, Tue 04 November 2025

---

Any callable [[Python programming language|python]] function that is used to modify a [[Function|function]], method or class
definition.

```python
@viking_chorus
def menu_item() -> None;
    print("spam")
```

is equivalent to.

```python
def menu_item() -> None:
    print("spam")

menu_item = viking_chorus(menu_item)
```

Decorators are merely used to make the code easier to read and express for
humans (syntactic sugar).

### See also:

[Wikipedia | Decorators](https://en.wikipedia.org/wiki/Python_syntax_and_semantics#Decorators)

