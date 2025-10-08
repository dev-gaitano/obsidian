---
id: 1759398350-NAET
aliases:
  - CSS Sticky Position
tags:
  - css
  - programming
  - styling
  - webdevelopment
status: adult
---

---

12:48, Thu 02 October 2025

---

# CSS Sticky Position

```css
{
position: sticky;
}
```

This is one of a few value that can be passed into the `position` attributes in
CSS.

This value allows an element to act like a relatively position until it reaches
a certain point, then it acts as a fixed element.

```css
{
position: sticky;
top: 30px;

/*
   This will make the element act relatively positioned until the page is
   scrolled to a point where there's 30 pixels above the element
*/
}
```

You can combine `position: sticky;` with the "scroll Index" to achieve an
intersesting sticking effect.

### See also:

[[Coding2GO - Learn CSS Positions in 4 minutes]]
[MDN Docs | CSS Layout Positioning](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Positioning)
