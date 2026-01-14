---
id: Hello World Program In C
aliases:
  - Hello World Program In C
tags:
  - c
  - programming
  - programminglanguage
status: adult
---

10:15, Mon 20 October 2025

---

# Hello World Program In C

In [[C]], to create a program to print "Hello, world!" we,

1. First, tell the program to include information about the standard
   input/output library;

```c
# include <stdio.h>
```

2. Then, define a [[Function|function]], `main` in this case.

```c
// type name(args) {}
int main(void) {}
```

The "main" function is a special function. Why? It is the entry point of the
program. This is the function that the system runs first before any other
function.

After running the `main` function, the operating system expects a numeric exit
code in order to determine if the program ran as intended. This is why we
declare the function's return type as an `int` because we expect integer to be
returned.

These exit codes can be;

- `0` for success
- Any other integer for some kind of error

You can also declare the exit code explicitly;

```c
int main(void)
{
  return 0;
}
```

Because our program won't require any ==arguments== to run, we could either leave
the parathesis blank, which the program will read as unknown arguments (not the
best practise) or use the `void` keyword to explicitly declare that no
arguments should be passed.

3. Call the `printf` library function and pass in the string "Hello, world!" as
   an argument.

```c
# include <stdio.h>

int main(void)
{
  printf("Hello, world!\n"); // print statement
  return 0 // optional
}
```

4. Compile and run the program.

### See also:

Book: The C Programming Language - Brian Kernighan & Dennis Ritchie
