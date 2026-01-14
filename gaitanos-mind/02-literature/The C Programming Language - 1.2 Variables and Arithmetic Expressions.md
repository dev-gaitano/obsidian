---
id: The C Programming Language - 1.2 Variables and Arithmetic Expressions
aliases:
  - 1.2 Variables and Arithmetic Expressions
tags:
  - c
  - programming
  - programminglanguage
status: child
---

20:49, Tue 28 October 2025

---

In this section, we are going to be using [[Variable|variables]] and 
arithmetic expressions ([[Arithmetic Expressions]]) to create a program that

converts Fahrenheit to Celsius.

The formula for changing Fahrenheit to Celsius is;

$$
c = \frac{5}{9}(f - 32)
$$

The program consists of a single [[Function|function]] - The main function.

```c
#include <stdio.h>

int main(void) {
    int fahr, celsius;
    int lower, upper, step;
    //NOTE: Why did we define these variables on different lines?

    lower = 0;
    upper = 300;
    step = 20;

    fahr = lower;
    while (fahr <= upper) {
        celsius = 5 * (fahr - 32) / 9;
        printf("%d\t%d\n", fahr, celsius);
        fahr = fahr + step
    }
}
```

## Variables

In C, all variables must be defined before they are used.

The definition announces the variable properties; the name and a list of
variables such as ==What do they mean by "name"?==

```c
    int fahr, celsius;
    int lower, upper, step;
```

The type `int` means that the variables listed are integers, while type `float`
means the variables listed are floating point - numbers that have a decimal part.

The range of both `int`s and `float`s depends on the type of machine you are
using, either a 16-bit, 32-bit or 64-bit.

C also has other data types, including:

| Data Type | Definition                      |
| --------- | ------------------------------- |
| char      | character - a single byte       |
| short     | short integer                   |
| long      | long integer                    |
| double    | double precision floating point |

==What is a double precision floating point?==

The size of these data is also machine dependent and there are several other
data types apart from the ones mentioned above.

Computation in the program starts with the assignment statements

```c
    lower = 0;
    upper = 300;
    step = 20;
```

This sets initial values to the variables.

## The `while` loop

The `while` loop can be one statement,

```c
while (x < y)
    i = 2 * i;
```

or multiple statements enclosed by curly braces, like in our temprature
converter program.

In this program, we use the `while` loop to repeat the same computation for each
Fahrenheit value if the condition in our brackets is met.

```c
    while (fahr <= upper) {
        ...
    }
```

How the `while` loop operates:

1. The condition in the brackets is tested.
   - Is `fahr` less than or equal to `upper`?

2. If the condition is `true`:
   - The body - The statements inside the curly braces - of the `while` loop is run.
   - The condition is retested, and if `true`, the body is run again.

3. If the condition is `false`:
   - The loop is broken and the program runs the statement after the loop. In
     this case, the program returns `0` to end the program.

Inside the body of the loop, the celsius temprature is computed and assigned to
the variable `celsius` by implementing our converion formula in the statement

```c
        celsius = 5 * (fahr - 32) / 9;
```

==The reason we are mulipliying by 5 the dividing by 9, intead of just
multipliying by 5/9 is beacuse in C, integer division truncates. 5/9 would be
truncated to zero.==

For the `printf` statement, its first argument is a string of characters to be
printed with each % acting as a placeholder for one of the other arguments and
specifing in what data type it belongs to. For example in this program, `%d`
specifies an interger is to be subsitituted.

The first % is always paired up with the second argument, then the second % to
the third argument and so on.

```c
        printf("%d\t%d\n", fahr, celsius);
```

This prints out the values stored in the variables `fahr` and `celsius` with a
tab (\t) between them.

**Program Improvements**

1. Give Each argument a width to have a more consistent alignment.

```c
        printf("%3d %6d\n", fahr, celsius);
```

this prints the first argument 3 digits wide and the second 6 digits wide.

2. Change the integer types to floating point. This allows the program toreturn
   a more accurate value.

```c
#include <stdio.h>

int main(void) {
    float fahr, celsius;
    float lower, upper, step;

    lower = 0;
    upper = 300;
    step = 20;

    fahr = lower;
    while (fahr <= upper) {
        celsius = (5.0/9.0) * (fahr-32.0);
        printf("%3.0f %6.1f\n", fahr, celsius);
        fahr = fahr + step;
    }
}
```

This version is almost identical to the `int` version, but note that here,
during our celsius calculation, we multiply by 5.0/9.0 because unlike `int` types
it's not truncated but instead it returns the ratio of the two floats.
==Is it because floats cannot be truncated?==

if an ==arithmetic operator== has one Floating point ==operand== and one Integer
operand, the Integer will be converted to Floating Point before the operation is
done.

The `printf` function explicitly specifies how many (if any) decimal points we
want to be printed out, `%f` and to print the number as a Floating Point.

```c
        printf("%3.0f %6.1f\n", fahr, celsius);
```

Below are some placeholders that `printf` recognizes;

| Placeholder | What it does                                                       |
| ----------- | ------------------------------------------------------------------ |
| %d          | print as decimal integer                                           |
| %6d         | print as decimal integer, at least 6 characters wide               |
| %f          | print as floating point                                            |
| %6f         | print as floating point, at least 6 characters wide                |
| %.2f        | print as floating point, 2 characters after decimal point          |
| %6.2f       | print as floating point, at least 6 wide and 2 after decimal point |

### See also:

[[C Programming Language|c Programming Language]]
