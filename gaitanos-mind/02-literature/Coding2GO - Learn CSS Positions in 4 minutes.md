---
id: Coding2GO - Learn CSS Positions in 4 minutes
aliases: []
tags: []
---

07:39 Sat 1st March 2025

Status: adult

Tags: #css #programming #programminglanguage #webdevelopment  #youtube

---

Source: https://youtu.be/YEmdHbQBCSQ?si=lZczUDKjv8-5tRoY
Author: Fabian - Full stack web developer

---

The position property in CSS ca assume 5 possible values;

```css
position: static; /* The default position the element should be in */
position: relative;
position: fixed;
position: sticky;
position: absolute;
```

While using the all the other position attributes apart from 'static' we can use properties to position our element right where we want it to be;

1. Top
2. Bottom
3. Left
4. Right
5. Z-index

#### 1. relative

When we use the 'relative' attribute we offset the element relative to its default position (static position).

```css
position: relative;
top: 30px;
left: 30px;
```

This will move the element 30 pixels from the top and 30 pixels from the left as well relative to its default position.

![[Pasted image 20250301083628.png]]

We can also use the right and bottom properties, depending on what we want to achieve in our design.

#### 2. fixed

This attribute will fixate the element to the window, this means if we have a scrollable design the element will stay fixed to the window and will not scroll with the other elements.

This attribute place the element in a separate layer above all the other elements.

```css
position: fixed;
top: 0;
right: 0;
```

Now the positioning properties will work differently compared to the relative attribute.

In this case, the element will be positioned 0 pixels from the top and right edges of the users screen.

![[Pasted image 20250301084427.png]]

With 'fixed' attribute we can also use percentages, for example,

```css
top: 50%;
left: 50%;
```

This will position the element's origin 50% from the top and left edge (relative to the screen).

![[Pasted image 20250301084722.png]]

To have position the element's center rather than the origin we have to introduce another property, the 'translate' property.

```css
translate: -50% -50%;
```

This means, translate the element -50% on the x-axis and -50% 0n the y-axis.
The fully centered element using the 'fixed' position attribute and percentages, should look something like this;

```css
position: fixed;
top: 50%;
left: 50%;
translate: -50% -50%;
```

![[Pasted image 20250301085450.png]]

_NB: This is what those annoying pop-ups use when the want you to accept the cookies_

#### 3. sticky

[[CSS Sticky Position]]

A sticky element behaves just like a fixed element, but not until it reaches a specified sticking point.

```css
position: sticky;
top: 0;
```

In this case, the element will stick when it reaches the position where the top is 0 pixels from the element.

#### 4. absolute

This attribute positions the element relative to it's nearest ancestor with position property.

For this example we need to define our HTML structure for better understanding.

```html
...
<body>
  <div class="parent">
    <h2>Parent Element</h2>
    <p>Lorem ipsum dolor sit amet con....</p>

    <div class="child">
      <h2>Child Element</h2>
    </div>
  </div>
</body>
...
```

```css
.parent {
  position: relative;
}
.child {
  position: absolute;
  top: 0;
  right: 0;
}
```

We are using the relative attribute as this attribute has no effect on the element if we don't add the positioning properties. ==Why not `position: static;`==

The child element will now be positioned 0 pixels from the top and right relative to the parent element.

![[Pasted image 20250301092057.png]]

This only works because we also have a position property in the parent element. If we were to remove the position property from the parent,

```css
.parent {
}
.child {
  position: absolute;
  top: 0;
  right: 0;
}
```

The child element would be positioned relative to the body as though we were using the 'fixed' attribute.

![[Pasted image 20250301092459.png]]

The absolute attribute positions the element in a separate layer from all the other elements in the parent element, meaning our element will be on top of all the other elements.

We can change the layer order of our elements using the 'z-index' property. If we assign negative values we put an element beneath all the others.

### See also:
