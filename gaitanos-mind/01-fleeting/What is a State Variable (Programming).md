---
id: What is a State Variable (Programming)
aliases:
  - state variable
  - setter function
tags:
  - definition
  - programming
status: child
---
---

11:46, Sun 01 March 2026

---

A state variable is a special variable, used in [[What is State Management (Programming)|state management]] to
retain/remember a variable's value between renders.

It is updated using a state setter function. This state setter function also
triggers a component re-render whenever the state variable is updated. 

An example of this implementation is React's `useState` hook.

### See also:

[React docs - State: A Component's Memory](https://react.dev/learn/state-a-components-memory)
