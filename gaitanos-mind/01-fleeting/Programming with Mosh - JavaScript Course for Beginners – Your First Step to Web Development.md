20:52 Mon 20th January 2025

Status: teen

Tags: #youtube #javascript #webdevelopment

------------------------------------
https://youtu.be/W6NZfCO5SIk?si=AkXorzoP0TrMkXQf
Mosh Hamedani - Youtuber
#### What is JavaScript?
It is a programming language.

It can used with both backend and frontend web development.

**Where does JavaScript code run?**
JS originally used to run only on browsers due to their inbuilt engines.

But Node - a ==C++ program== that includes googles V8 engine - allows JS to run outside the browser. This allows Devs to build the backend of the browser using JS.

Browsers and Node provide a ==runtime environment== for JS.

**What is the difference between JavaScript and ECMAScript?**
ECMAScript - A specification.
JavaScript - A programming language that adheres to this specification.

We can try out JS code in the browser's Dev tools
![[Pasted image 20250120211106.png]]


#### Setting Up the Development Environment
1. You need a code editor - we are going to be using vscode in this tutorial.
2. Node.js - This is not compulsory as you can run JS through the browser, but it is used when installing third party libraries. 
3. Create a new project directory.
4. Create an 'index.html' file in the project directory.
5. While in the HTML file, add the HTML boiler plate using the symbol '!' then enter or tab.
6. Install the Live Server extension for vscode.
7. Open your HTML file with Live Server by right clicking on the file and selecting the option 'Open with live server'.![[Pasted image 20250120212714.png]]


#### JavaScript in Browsers
There are two places we can add our script element in our HTML file:
1. In the head section
2. In the body section

The best practice is to put it in the body section after all the existing elements. (There are exceptions where it is better to put it in the header)

This is because the browser reads the HTML document from top to bottom, and we want it to parse our HTML elements first. Why?

1. If it parses the script first it may generate some lag on the client-side before actually displaying the contents of the page, creating a bad user experience.
2. Our script will work with the data from the previous elements. Loading those elements first will make the communication between the elements and our script more efficient.

We add the script element using the script tag `<script></script>`.

Let's add our first command to the script element
```
<script>
	// This is my first JavaScript code
	
	console.log('Hello World!');
</script>
```
This tells JS to 'log' on the 'console' the string 'Hello World!'

All JS commands must be finished / closed with a semi-colon (;).

In JS commands are referred to as statements.

The two forward slashes refer to a comment in JS. Comments should be used to describe the purpose of the code not the function of the code, because the code should be clear enough to understand.


#### Separation of Concerns
Ideally we want to separate our JS code - which is about the site's behavior - and our HTML code - which is about the structure of the site.

This separation of code is what we refer to as 'Separation of Concerns'.

To do this we:
1. Create a new file called 'index.js', in our project directory.
2. Cut the code from our script element and paste it into our 'index.js' file.
```
index.js

// This is my first JavaScript code
console.log('Hello World!');
```
3. Reference our JS file in our HTML file.
```
index.html

<script src="index.js"></script>
```


#### JavaScript in Node
Run the following command in the terminal in your project directory,
```
node index.js
```
then press enter.

This will return the same output as our browser which is,
```
Hello World!
```


#### Variables
Variables are used in programming to store data temporarily to the computers memory.

We give the variables names in order to be able to read the data in future.

A variable is like a labelled box with or without items (data) in it.

Today in JS, variables are declared using the keyword `let` , but before 2015 they were declared using the keyword `var`. ==Why was is it changed? Had a lot of limitations==

Here is an example of a JS variable

```
index.js

let name;
```

'name' - identifier / name of the variable / label of the box

To see the output we have to log the variable to our console.
```
index.js

let name;
console.log(name)
```
the output of our log will be 'undefined' because we have not defined the data / item in our variable.
![[Pasted image 20250120230849.png]]

To define the data we,
```
index.js

let name = 'Mosh';
console.log(name)
```
This will log the string 'Mosh' into our console.
![[Pasted image 20250120231138.png]]

There are a few rules that apply when choosing a name for your variable:
1. Cannot be a reserved keyword, e.g. let.
2. Should be meaningful and descriptive. Should give a hint of the data being stored.
3. Cannot start with a number.
4. Cannot contain a space or a hyphen (-), use camelCase instead.
5. The names are case sensitive.


#### Constants
Constants also store data like variables for future reference, but the data in them can not be changed / reassigned. It is constant, hence the name **CONSTANT**.

With constants we use the keyword `const` instead of `let` when declaring them
```
index.js

const interestRate = 0.3;
console.log(interestRate)
```

If we try reassigning different data to the constant, we will get an error in our console, e.g.
```
index.js

const interestRate = 0.3;
interestRate = 1;
console.log(interestRate)
```

![[Pasted image 20250120233204.png]]


#### Primitive Types
Data types are the kinds of values that we can assign to variables.

In JavaScript we have two kinds of types:
1. Primitives / Value types.
	1. String
	2. Number
	3. Boolean
	4. Undefined
	5. Null
2. Reference types.
	1. Objects
	2. Arrays
	3. Functions

In this section we are going to be focusing on the primitive types.

```
let name = 'Mosh'; // String Literal
let age = 30; // Number literal
let isApproved = true; // Boolean literal
let firstName; // Undefined literal
let lastName = null; // Null literal - used in situations where we want to clear the value of a variable
```


#### Dynamic Typing
We have two types of programming languages
1. Static - Statically-typed
2. Dynamic - Dynamically-typed

In static languages, the data type of the variable is set and cannot be changed in future.

In dynamic languages, the data type of the variable can be changed in future.

JavaScript is dynamically typed.

Let's assume we have a variable `name`
```
let name = 'Mosh';
```

To check the type of the variable we use the keyword 'typeof'
![[Pasted image 20250121115920.png]]
We can see that the type is 'string', but with JS this can be changed dynamically.

![[Pasted image 20250121120033.png]]
![[Pasted image 20250121120143.png]]
After changing the name value to be '1' we can now see the type has been dynamically changed to 'number'.


#### Objects
Objects fall under the reference type of data type.

Inside an object type we have multiple properties / key-value pairs defined.

To define an object type we use the curly braces '{}'.
```
let person = {
	name: 'Mosh', // 'name' is the key, and 'Mosh' is the value, forming a key value pair
	age: 30
};
```

If we `console.log` our `'person'` object this will be the output,
![[Pasted image 20250121121359.png]]
![[Pasted image 20250121121445.png]]

There are two ways to work with the object type:
1. With the dot notation
	`person.name = 'John'`
2. With the bracket notation
	`person['name'] = 'John'`

The dot notation is more concise and is usually the go-to option in most cases.

The bracket notation is used when the key is selected during runtime, and / or is not known during the time of writing the code.

The Bracket notation allows the key to be selected dynamically.
```
// The selection variable is being selected during runtime

let selection = 'name';
person[selection] = 'Mary'
```


#### Arrays
We use arrays to store data in a list.

To define an array in JS we use the square brackets '\[]' 
```
let selectedColors = ['red','blue']
```

If we log our array object onto the console,
```
console.log(selectedColors)
```
we'll see
![[Pasted image 20250122091031.png]]

Every array item has an index, with zero being the index for the first item in the array.

If we want to display a specific item in our array we use its index
```
// Selecting the first item in our array

console.log(selectedColors[0])
```
this will return
![[Pasted image 20250122091337.png]]

JS being dynamically typed we can also add items to an existing array.
```
// Adding a new item to our array

selectedColors[2] = 'green'
```
This will add 'green' to our second index in our array.

If we log our array object onto the console,
```
console.log(selectedColors)
```
we'll see green has been added to our array object
![[Pasted image 20250122091929.png]]
This shows that in JS array objects' lengths are dynamic. 

In JS, every item stored in the array object doesn't have to be of the same data type, we can have an array with multiple data types mixed together. For example,
![[Pasted image 20250122092238.png]]


#### Functions
These are a set of statements that perform a task or a calculation.

To declare a function we use the `function` key word, then the 'function name' followed by brackets - () - then we put the body of the function - the set of statements - inside a pair of curly braces ({}) .
```
// A function performing a task

function greet() {
	console.log('Hello World');
}
```
we do not end a function with a semi-colon (;), like a variable.

After declaring a function, for it to run we have to call it. We type the name of the function followed by brackets and a semi-colon (;).
```
greet();
```
This is what we should have on the console after running our 'greet' function.
![[Pasted image 20250122103304.png]]

Functions can have inputs that change how the function behaves.

To add an input we need to add a parameter between the brackets after the function name while declaring the function.
```
function greet(name) {
...
```
then we add the parameter to our function body.
```
function greet(name) {
	console.log('Hello ' + name)
}
```

While calling the function we pass the input as an argument
```
greet('John');
```

This will return our input
![[Pasted image 20250122103951.png]]

The function can now be repeated but with different inputs. For example,
```
greet('John');
greet('Mary');
```
![[Pasted image 20250122104142.png]]

A function can also have more than one parameter. Parameters are separated using commas. For example,
```
function greet(firstName, lastName) {
...

greet('John', 'Smith');
```
![[Pasted image 20250122104631.png]]

#### Types of functions
The previous function was performing a task, but we can also use functions to make calculations.

```
// Calculating a value
function square(number) {
	return number * number;;
}

console.log(square(2));
```
![[Pasted image 20250122105601.png]]

We can also use functions inside a variable instead of calling it directly. We need to add a 'return' keyword to our function statement in the body.
```
function square(number) {
	return number * number;
}

let number = square(2);
console.log(number);
```
This will give us the same output.
![[Pasted image 20250122105745.png]]


### See also:
[[JavaScript]]
[[CS50x 2024 - Lecture 8 - HTML, CSS, JavaScript]]