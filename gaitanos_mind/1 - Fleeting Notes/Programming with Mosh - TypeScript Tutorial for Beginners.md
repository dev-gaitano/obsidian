01:31 Sat 22nd February 2025

Status: child

Tags: #typescript #webdevelopment #programminglanguage #youtube 

------------------------------------
https://youtu.be/d56mG7DezGs?si=JeP_ONVnqqWR-833
Mosh Hamedani - Youtuber

## SECTION 1 : INTRO
### 1. Introduction to TypeScript

**What is TypeScript?**

A programming language to solve some of JavaScript's shortcomings. A disciplined sibling of [[JavaScript]].
Anything we can do with JavaScript we can do with TypeScript.

**Why do we need it?**

TypeScript is JavaScript with type checking, helps us catch our mistakes before runtime by compiling our application.

**How is it different from JavaScript?**

TypeScript offers more than just type checking:
![[Pasted image 20250222014230.png]]

One drawback of using TypeScript is that, TypeScript code has to undergo a process called 'Transpilation' to convert it to JavaScript before running on the browser.==Why?==


### 2. Setting Up the Development Environment

1. Download Node.js.
2. Install the TypeScript compiler globally using npm(Node Package Manager).

```bash
npm i -g typescript
```

To confirm if the installation was successful, check the TypeScript Compiler(tsc) version using,

```bash
tsc -v
```

If the installation was successful, this should return the version you installed.


### 3. Creating Your First TypeScript Program

1. Create a new project directory anywhere on your pc(pick whatever name you want) and open it in your code editor of choice, e.g. Vim

``` bash
mkdir hello-world
```
```bash
vim hello-world
```

2. Create a new TypeScript file using the '.ts' extension, with the name 'index'.

```bash
touch index.ts
```

3. Open the TypeScript file and write some basic JavaScript code. For example,

```typescript
console.log('Hello World')
```

All JavaScript syntax can work in Typescript.

4. Open the terminal, then compile the code using the TypeScript compiler.

```bash
tsc index.ts
```

This will create an identical JavaScript version of our TypeScript file. This process of turning the code to JavaScript is what we call 'Transpilation'.

5. Back in your 'index.ts' file, declare the variable 'age',

```typescript
let age: number = 10
```

In TypeScript we can add text notations. These notations tell the compiler what data type the variable value should be, In our case the data type is number.

If we try to reassign the variable with a value that does not belong to the number data type, the TypeScript compiler will output an error. For example,

```typescript
age = 'Gaitano'
```

![[Pasted image 20250222025437.png]]

*NB: This allows us to catch errors way before runtime(during compile time), saving time.*

If a variable is reassigned, the value should always be of the same data type as the one we declared in the text notation.

```typescript
age = 20
```

6. Compile you TypeScript code again, using command 'tsc'. In your 'index.js', the 'let' keyword that we used to declare the variable will have been changed to 'var',

```javascript
var age = 10
```

This occurs because the TypeScript compiler defaults to ES5 which is an older JavaScript specification. To use the latest specification, we have to configure it ourselves.


### 4. Configuring the TypeScript Compiler

To configure TypeScript we need a configuration file. We create the file using the terminal command,

```bash
tsc --init
```

This will create a file 'tsconfig.json', in our project directory.

After opening the config file you will see a long list of all possible configurations we can implement - you don't have to know all of them. Some of the more common ones are:

```json
/* Language and Environment */
"target": "ES2016",              /* Choose EcmaScript specification version */
...

/* Modules */
"module": "commonjs",
"rootDir": "./src",              /* Source Code Folder*/
...

/* Emit */
"outDir": "./dist",              /* Distributable Code Folder */
"removeComments": true,          /* Remove comments from dist code */
"noEmitOnError": true,           /* Only compile code if there are no errors */
...
```

All configuration options have comments to the side that explain its purpose.

With the new config setup, we can now compile our code without any arguments

```bash
tsc
```

TypeScript will now automatically know where to store all the distributable code and where all the source code is stored.

![[Pasted image 20250222100421.png]]


### 5. Debugging TypeScript Applications

Inside our 'tsconfig.json' file, enable,

```json
/* Emit */
"sourceMap": true,
...
```

This feature specifies how each line of our TypeScript code maps to the generated JavaScript code.

When we compile our code a new file will be created in our 'dist' directory - 'index.js.map', this file's syntax is not for us to understand but for debuggers.


## SECTION 2 : FUNDAMENTALS
### Built-In Types

TypeScript has all the primitive JavaScript data types, but it also adds some more types of its own. These added types are:
	1. Any
	2. Unknown
	3. Never
	4. Enum
	5. Tuple

In TypeScript we don't have to notate the type of primitive, the compiler will automatically detect the type based on the value provided.

```typescript
// Using text notation
let sales: number = 123_456_789;
let course: string = 'TypeScript';
let is_published: boolean = true;
```
```typescript
// Or not

let sales = 123_456_789;
let course = 'TypeScript';
let is_published = true;
```

Both examples are correct in this case.


### 1. The 'any' type

When we declare a variable and don't assign a value to it, the compiler will assume the data type any.

```typescript
let level; // Data type 'any'
```

This variable can later be assigned a value of any data type.

```typescript
level = 1
level = 'a'
```

But, using the any type defeats the main reason of using TypeScript, which is the strict implementation of variable data types.


### 2. Arrays

In TypeScript, all array values have to be of the same data type. For example,

```typescript
let numbers = [1, 2, 3]  // All values are numbers
```
```typescript
numbers[3] = '4'  // Will return an error because value is a string
```
```typescript
numbers[3] = 4   // Will work perfectly fine, because value is number
 ```

Just like with primitive data types, if we don't assign values to the array, the compiler will assume 'any'.

```typescript
let numbers = [];

numbers[0] = 1;  // Works!
numbers[1] = '2';  // Works!
numbers[2] = true;  // Works!
```

If we want to specify the data type for an empty array, we need to use a notation.

```typescript
let numbers: number[] = [];
```


### 3. Tuples

This is a fixed length array where each element has a particular type. It usually contains only two values / a pair of values.

```typescript
// 1, 'Gaitano'

let user: [number, string] = [1, 'Gaitano'];
```

Avoid having more that two values, as it makes the code confusing.


### 4. Enums

Enums represent a list of related constants.

```typescript
// const small = 1;
// const medium = 2;
// const large = 3;

// PascalCase for the enum name
enum Size { Small, Medium, Large};
```

By default, TypeScript automatically assigns the value zero '0' to the first member, then auto-increments for the other ones.

You can explicitly set the values.

```typescript
enum Size { small = 1, medium, large}; // medium becomes 2 & large 3
```
```typescript
// Or set a string value
enum Size { small = 's', medium = 'm', large = 'l'};
```

We can then declare a variable using the Enum 'Size',

```typescript
let mySize: Size = Size.medium; // Returns the value set to 'Medium'
```

To make the JavaScript version of the Enum setup more compact / optimized, we use the 'const' key word before the 'enum' keyword,

```typescript
const enum Size { Small, Medium, Large};
let mySize: Size = Size.medium;
```

```javascript
// JS file before adding 'const' keyword

var Size;
(function (Size) {
	Size[Size["small"] = 0] = "small";
	Size[Size["medium"] = 0] = "medium";
	Size[Size["large"] = 0] = "large";
})(Size || (Size = {}));
let mySize: Size = Size.medium;
```
```javascript
// JS file after adding 'const' keyword

let mySize = 1;
```


### 5. Functions

Let's look at how TypeScript can be implemented inside a function. We'll start by defining a function.

```typescript
// Define a function
function calculateTax(income: number) {
} // Returns type 'void'
```

```typescript
// Return a value
function calculateTax(income: number) {
	return 0;
} // Automatically assigns type 'number'
```

```typescript
// Explicitly notate function return type - Good Practice!
function calculateTax(income: number): number {
	return 0;
}
```

```typescript
// If we try to return a different type from the one we notated we get an error
function calculateTax(income: number): number {
	return 'a';
}
```

```typescript
function calculateTax(income: number): number {
  if (income < 50000) {
    let tax: number = income * 0.012;
    return tax;
  }
}
```

```typescript
function calculateTax(income: number): number {
  if (income < 50000) {
    let tax: number = income * 0.012;
    return tax;
  }
  let tax: number = income * 0.03;
  return tax;
}

console.log(calculateTax(20000)); // You can only pass a value type 'number' as an argument
```

```typescript
// Added another parameter
function calculateTax(income: number, tax_year: number): number {
  if (tax_year >= 2022) {
    if (income < 50000) {
      let tax: number = income * 0.012;
      return tax;
    }
    let tax: number = income * 0.03;
    return tax;
  }
  if (income < 50000) {
    let tax: number = income * 0.008;
    return tax;
  }
  let tax: number = income * 0.012;
  return tax;
}

console.log(calculateTax(20000, 2020)); // You can only pass two agruments 
```

```typescript
// Making a parameter optional
// Provided a default value for the taxyear
function calculateTax(income: number, tax_year = 2022): number {
  if (tax_year >= 2022) {
    if (income < 50000) {
      let tax: number = income * 0.012;
      return tax;
    }
...
console.log(calculateTax(20000, 2020)); // The argumentpassed will overide the default one
```

Add configurations to improve the TypeScript function experience.

```json
/* Type Checking */
...
"noUnusedParameters": true,
"noImplicitReturns": true,
"noUnusedLocals": true,
...
```


### 6. Objects


### See also: