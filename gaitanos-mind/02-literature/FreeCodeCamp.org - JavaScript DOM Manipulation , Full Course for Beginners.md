09:37 Sat 25th January 2025

Status: child

Tags: #javascript #dom #programminglanguage #youtube

------------------------------------
https://youtu.be/5fb2aPlgoys?si=lGatJkmvorzfSF__
Code Lab

#### What is the DOM?
Stands for the Document Object Model.

The DOM has many methods that be used to manipulate the content on our page.

This is one of the most unique and useful tools in the [[JavaScript]].

Think of the DOM as a tree with branches,
![[Pasted image 20250125095415.png]]

Objects in this model have a family - Parent, Child, sibling - relationship.

The 'Document' node is the root element that we use to access the DOM.

Classes and Ids are also present in this model but they don't follow the traditional family relationship like the other nodes do.


#### Selecting Elements in the DOM
```
index.html

...
<body>
	<div class="containerMovies">
		<h1 id="main_heading">Favourite Movie Franchise</h1>
		<ul>
			<li class="list_items">The Matrix</li>
			<li class="list_items">Star Wars</li>
			<li class="list_items">Harry Potter</li>
			<li class="list_items">Lord of the Rings</li>
			<li class="list_items">Marvel</li>
		</ul>
	</div>
	<script src=".script.js" async defer></script>
</body>
```

To manipulate an element, we first need to select the element. There are multiple ways we can do this, the five major ones are:
1. `getElementById()` - Returns the element in the document with the specified ID.
2. `getElementsByClassName()` - Returns all the elements in the document belonging to the specified class, in the order that they appear in the HTML document.
3. `getElementsByTagName()` - Returns all the elements in with the specified tag, in the order that they appear in the HTML Document.
4. `querySelector()` - Returns the first element in the HTML document with the specification given..
5. `querySelectorAll()` - Returns all the elements in our HTML document with the specification give. In the order that they appear in the HTML document.

*NB: `querySelector() && querySelectorAll()`  can grab elements in the HTML Document using any attribute - Class, Id, Tag, ... -*

```
script.js

// getElementByID() - This is the easiest way to select an element

document.getElementById('main_heading');

// To manipulate the selected element, we place the model into a variable

const title = document.getElementById('main_heading')

console.log(title) // This will log the element onto our console

```

```
script.js

// getElementsByClassName()

const listItem = document.getElementsByClassName('list_items');

console.log(listItem);
```

```
script.js

// getElementsByTagName()

const listItems = document.getElementsByTagName('li');

console.log(listItems);
```

```
script.js

// querySelector()

const container = document.querySelector('div')

console.log(container)
```

For `querySelectorAll()`, we need to add an extra 'div' to our HTML Document to see the selection done.

```
index.html

...
	<div class="containerSports">
		<h1 id="sports_heading">Favourite Sport Franchise</h1>
		<ul>
			<li class="list_items">NBA</li>
			<li class="list_items">UEFA</li>
			<li class="list_items">NFL</li>
			<li class="list_items">Formula One</li>
			<li class="list_items">WRC</li>
		</ul>
	</div>
...
```

```
script.js

// querySelectorAll()

const containerAll = document.querySelectorAll('div')

console.log(containerAll)
```

This will return all 'divs' in our HTML Document.

#### Styling an Element

### See also: