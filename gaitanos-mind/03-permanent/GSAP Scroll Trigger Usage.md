---
id: Scroll Trigger Usage
aliases:
  - Scroll Trigger Usage
tags:
  - gsap
  - gsap-plugins
  - libraries
  - webdevelopment
  - javascript
  - typescript
status: adult
---

14:10, Fri 08 October 2025

---

# Scroll Trigger Usage

[[GSAP Scroll Trigger]] a GSAP plugin allows anyone to create scroll-based animations using
the GSAP Library. [[GSAP Plugins]]

It offers;

- Scrub
- Pinning
- Snapping
- Trigger (Anything scroll-based, not necessarily animations)

Here is one simple example;

```jsx
// Register ScrollTrigger plugin
gsap.registerPlugin(ScrollTrigger);
```

1. Use the gsap `.to()` method

```jsx
gsap.to();
```

2. Pass in two arguments into the method,
   - The target element (Using CSS selectors)
   - An object to define attributes you want to pass onto the target element

```jsx
gsap.to(".box", {});
```

3. In the second argument object, pass in the target value into the `scrollTrigger` key and any other attributes you need to achieve your desired your effect

```jsx
gsap.to(".box", {
  scrollTrigger: ".box",
  x: 500,
});
```

For this example code, when an element with the class `.box` comes into view, it will slide 500 pixels to the positive x axis (to the right).

### See also:

[[GreenSock Animation Platform (GSAP) library]]
[[GSAP Learning - Introducing ScrollTrigger for GSAP]]
