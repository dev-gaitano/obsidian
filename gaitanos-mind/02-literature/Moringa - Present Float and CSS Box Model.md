---
id: Moringa - Float and CSS Box Model Present
aliases: []
tags:
  - moringaschool
  - webdevelopment
  - css
  - programming
status: adult
---
---

12:29, Tue 04 November 2025

---

## Float

What is a Float?
A float is a CSS declaration

What is a CSS declaration?
These are rules that define how a specific HTML element should be styled.
```css
p {
	font-size: 20px;
	font-weight: bold;
	color: red;
	float: right;
}
```

What does a float do?
In HTML each element comes after the other.

Float declarations are used to allow us, the developer, to wrap these elements around each other in our website.

For example,
(I am assuming you have already created your HTML and CSS files)

1. Create HTML boiler plate
2. Create image add id
3. Create paragraph
4. Link style sheet
5. Wrap text around image
6. Create a second image
7. Add another paragraph
8. Wrap text around second images

```html
<!-- index.html -->

...
<img src="example.jpg" alt="Wrapped Image">
<p>We want to wrap this text around our image</p>
```

```css
/* css/style.css */

...
img {
	float: left;
}
```

Floats can also be used to create columns in our website

```html
<!DOCTYPE html>
<html>
  <head>
    <link href="css/styles.css" rel="stylesheet" type="text/css" media="all">
    <title>Columns</title>
  </head>
  <body>
    <h1>Let's see some columns!</h1>
    <div class="column">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
    </div>
    <div class="column">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
    </div>
    <div class="column">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
    </div>
  </body>
</html>
```

```css
.column {  
  width: 350px;  
  float: left;  
}
```

## CSS Box Model

What is the box model?
What does it do?
Why is it important?

All elements in CSS are a box either rectangular or square.

Content - The element
	Padding - add background to an element.
		Border - add a border around the element
			Margin - space two elements apart from each other

```css
* {
    padding: 0;
    margin: 0;
    font-size: 40px;
}

.box-one {
    background-color: #EB5757;
    padding: 10px;
    height: 100px;
    width: 100px;
    border: 30px solid #9B51E0;
    margin: 60px;
}

.box-two {
    background-color: #2D9CDB;
    border: 0 solid #27AE60;
}

```
