---
id: Corey Schafer - Python Tutorial for Beginners 2, Strings - Working with Textual Data
aliases: []
tags:
  - python
  - programminglanguage
  - programming
  - youtube
Author: Corey Schafer - YouTuber
Source: https://youtu.be/k9TUPpGqYTo?si=5XbqQpQ-lcbpgeUu
status: child
---
---

09:31, Sun 9th March 2025

---

Textual data in python is represented with strings.

In [[Corey Schafer - Python Tutorial for Beginners 1, Install and Setup for Mac and Windows]], we created a file 'intro.py' with a print function that holds a text value.

![[intro.py]]

```python
print('Hello World')
```

We can alternatively let a variable hold our text value, then pass in the [[Variable|variable]] name into our print function instead;

```python
# 'message' is our variable name
message = 'Hello World'

print(message)
```

This will print the same result as the first one, which is;

```bash
Hello World
```

In python, variable names are usually lower case and if it has multiple words they are separated by an underscore, for example;

```python
# Variable name with multiple words
my_message = 'Hello World'
```

In python, strings can not only be represented with single quotes (' '), but also double quotes (" ");

```python
# Using double quotes
message = "Hello World"
```

In this case, both the single and double quotes work equally as well, but there are certain times where it would be ideal to use the double quotes over the single quotes;

```python
# When there is an apostrophe in the text value
message = "Bobby's World"
```

If we use single quotes in the above example, python will treat the apostrophe as a closing quote causing an error when we run the code.

```python
# This will return an Error
message = 'Bobby's Message'
```

If we wanted to use the single quotes in the above case, for whatever reason we can use a backslash before the character we want python to ignore;

```python
# Use a backslash to ignore the apostrophe
message = 'Bobby\'s World'
```

The backslash will ensure that the apostrophe doesn't close out the string.

This logic goes both ways, if you know that your string contains double quotes in it, it would be ideal to use single quotes to open and close the string, or use the backslash to ensure that the double quotes in the string doesn't close out the string.

To store a string with multiple lines in python we use three quotes before and after the string either double or single quotes depending on the type of text represented in your string;

```python
# A multi-line string
message = """Bobby's world was a good
cartoon back in the 1990s"""
```

Python treats every single character in our string as an individual character.

To get the number of characters we have in our string we use the `len` function;

```python
message = "Hello World"

print(len(message))
```

If we run our code, python will print the length of our string / the number of characters;

```bash
11
```

*NB: The `len` function treats spaces as characters as well*

We can also access characters individually from our string by using the square bracket notation '\[ ]'.

```python
print(message[])
```

Inside the square bracket we place a number, known as an index. The index is the position of the character in the string. This allows python to know the character we want to access from the string.

The first character has an  index of '0'. In our case, if we want to access H - our first character - we pass in the index zero into our square bracket;

```python
print(message[0])
```

This will print our first character in the string represented by the message variable;

```bash
H
```

To access the last character, we can either use its actual index number - which in our case is 10 - or use '-1', this tells python to get the character with the index of 

$$
total string length - 1
$$

which in our case is still 10, because our string length was 11.

```python
print(message[10])

# or

print(message[-1])
```

returns;

```bash
d
```

If we try to access an index that does not exist, python will throw an error;

```python
# This will throw an error
print(message[11])
```

We can also access a range of characters by using a colon ':'.

Let's assume we want to only access the 'Hello' part of the string

```python
# Accessing a range of characters in a string
print(message[0:5])
```

While accessing a range of characters, the first index passed is included but the last one is not. What do I mean?

What the colon does is that it tells python, "I want the characters from the index 0 up to but not including index 5"

The print result for the above statement will be;

```bash
Hello
```

If we are starting our range from the start of the string we can leave out the first index value and python will automatically assume we want to start our range from the beginning of the string;

```python
print(message[:5])
```

This also works when we want to access a range of characters from a certain point to the end of the string;

```python
print(message[6:])
```

Print result;

```bash
World
```


#### String Methods

A method is a function that belongs to a specific object.

Methods add a lot of useful functionality to our objects.

Let's assume we want all our characters in our message string to be lowercase, we can use the `lower` method;

```python
message = 'Hello World'

# Lowercase Method
print(message.lower())
```

The print result will be;

```bash
hello world
```

To uppercase;

```python
# Uppercase method 
print(message.upper())
```

The print result will be;

```bash
HELLO WORLD
```

If we wanted to count the number of times a specific character appears in our string, we use the `count` method and pass the character we want to count as an argument, so that python knows what to count;

```python
print(message.count('l'))
```

This will return;

```bash
3
```

Because 'l' appears three times in our 'Hello World' string.

### See also:
