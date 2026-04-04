---
id: Presentation - High Order Functions
aliases: []
tags: []
status: child
---
---

15:50, Tue 31 March 2026

---

## What are high order functions?

High order functions are functions that take other functions as arguments,
or return them as results when it's done.

High order functions treat functions as values.

## Why would a function take another function as an argument?

To perform an action on it or with it

This is because it is difficult to define what we want the function to do with
the parameter with a primtive data type e.g int, str.

```javascript
// First order fumction
function double(n) {
    return n * 2;
}
```

An example of a high order function os the array filter method.

With the filter function it we can't be able to define our filtering criteria
with just a primitive type.

```javascript
// High order function
const names = [ "Sara", "Jay", "Pato", "Quinta", "Gaitano", "Mitchell" ]
names.filter(name => name[0] !== "Q")
```

```javascript
names.filter(
  function (name) {
    if (name[0] === "Q") {
      return false
    }
    return true
  }
)
```

```javascript
```

Another example of a high order function is the `map()` method.

```javascript
const nums = [ 1, 2, 3, 4, 5 ]
nums.map(num => num * 2)
```

Or we could pass in the `double()` first order function we defined at the start,

```javascript
const nums = [ 1, 2, 3, 4, 5 ]
nums.map(double)
```

`sort()`

Sort automatically treats the array items as strings and sorts them in ascending
order.

```javascript
array.sort((a, b) => a - b)
```

How does this work?

This function iterates over an array selecting a pair of items and checkig if
their subtraction returns a positive number.

If the result is positive the first number comes first, if not it swaps the
methods.

`reduce()`

reduces an array to a single value. ==Can it be used with string arrays?==


## Why would a function return another function as a result?

We want to get data that is not readily available.

```javascript
function login(retrieveUserData){
    const user = retrieveUserData();

    function greetUser(user){
        return `Welcome ${user.name}!`;
    }

    return greetUser;
}
```

## Why use high order functions?

- Allows one to reduce the rewriting/repeating repetitive functions, e.g filter
- These functions are smaller (Abstract) making for easier testing and debugging.
- Makes code-base more readable

## How to use them to our advantage

### See also:

