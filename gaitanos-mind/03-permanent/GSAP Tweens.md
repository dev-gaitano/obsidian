---
id: GSAP Tweens
aliases:
  - GSAP Tweens
tags:
  - gsap
  - gsap-methods
  - libraries
  - webdevelopment
  - javascript
  - typescript
status: adult
---

16:29, Fri 10 October 2025

---

# GSAP Tweens

In GSAP, Tweens do all the animation work.

You feed in;

- "targets" - These are the objects you want to animate,
- The duration of the animation,
- The properties that you want it to animate.

There are three main methods to create Tweens;

```jsx
gsap.to();
```

This method is used when you want to animate the target from the current value to
a specified value.
It's like telling the target, "You are here, move over there."

```jsx
gsap.from();
```

Used when you want to animate the target from a specified value to the current
value.
It's like telling the target, "Pretend you were there, then settle here"

```jsx
gsap.fromTo();
```

Used when you want to specify both the starting value and the end value. This
option offers the most control over your animations.
"Start at this value, then finish exactly at that value"

### See also:

[GSAP Docs](https://gsap.com/docs/v3/GSAP/Tween)
[[GreenSock Animation Platform (GSAP) library]]
