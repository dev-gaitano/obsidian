13:04 Sun 9th March 2025

Status: adult

Tags: #css #programminglanguage #youtube #webdevelopment #programming 

---
https://youtu.be/dIUOWdwwZBw?si=vVyPJBqvjQmaWF0r

---
::before and ::after are pseudo elements created using CSS.

When creating a HTML element you usually have an opening tag, a closing tag and content in-between;

```html
...
<h1>My Element</h1>
```

When addressing the element in CSS, think of the before and after properties as inserting a non-existent element either before or after your element content respectively;

```css
/* Inserts pseudo element before content */
h1::before {
}
```
```css
/* Inserts pseudo element after content */
h1::after {	
}
```

Using these properties allows us to style and manipulate these non-existent elements just like all the other elements in our HTML file.

Because these elements don't exist in your HTML, you have to define everything in CSS, including the content;

```css
h1::before {
	content: 'Hello';
}
```

![[Pasted image 20250309132248.png]]

If your pseudo element is only needed for design purposes, there is no need to put text into the content field. Despite this, you still need to have the content field present even if you are not going to put content in it;

```css
h1::before {
	content: '';
}
```

When using an empty string in the content property, we need to add a position property and depth using the height and width properties to our pseudo element in order to interact with it, or else any styling we add to it won't be visible;

```css
h1::after {
	content: '';
	position: relative;
	height: 10px;
	width: 10px;
	background: red;
}
```

![[Pasted image 20250309133139.png]]

Let's create a pseudo element that underlines our entire h1 element;

```css
h1 {
	position: relative;
	width: max-content;
}
h1::after {
	content: '';
	position: absolute;
	background: red;
	height: 4px;
	width: 100%;
	bottom: 0;
	left: 0;
}
```

![[Pasted image 20250309133717.png]]

The main advantage of using ::before and ::hover properties is that we have the entire power of CSS on our side because it treats these elements just like regular HTML elements.

We can add gradients, border radii, hover properties, etc. ;

```css
h1 {
	position: relative;
	width: max-content;
}
h1::after {
	content: '';
	position: absolute;
	background: linear-gradient(to right, red, blue);
	border-radius: 2px;
	height: 4px;
	width: 100%;
	bottom: 0;
	left: 0;
}
h1:hover::after {
	width: 0;
}
```

![[Pasted image 20250309134350.png]]

With CSS pseudo elements, your creativity is the limit.
### See also:
[[Coding2GO - Learn CSS Positions in 4 minutes]]