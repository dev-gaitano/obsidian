---
id: GSAP Timelines
aliases:
  - GSAP Timelines
tags:
  - gsap
  - libraries
  - webdevelopment
  - javascript
  - typescript
status: adult
---

09:51, Tue 14 October 2025

---

# GSAP Timelines

GSAP timelines act as containers for Tweens. [[GSAP Tweens]]

After you create animations using Tweens, you use timelines to sequence and
position the animations.

Objects in the timeline are referred to as ==timeline children==.

Timeline children can not only be Tweens, but also other Timelines nested into a
bigger timeline.

To use timelines, we use the `.timeline()` GSAP method.

```jsx
gsap.timeline();
```

For readability, timelines are usually defined as a variable;

```jsx
const tl = gsap.timeline();
tl.to(".green", {x:100px, duration:1}) // Notice the lack of a semi-colon
  .to("red", {x:200px, duration:2})
  .to(".blue", {y:400px, duration:1});
```

These Tweens will be sequenced one after the other, starting with the green one,
then the red one and lastly the blue one.

However, timeline children don't have to come one after another, they can overlap. This can be done using an optional argument that you can add to the timeline child, **the Positional Argument**.

A number sets the absolute time (in seconds) that the animation starts;

```jsx
tl.to(".green", {x:100px, duration:1}, 0.5)
```

This will ensure that the "green" target's animation always starts after 0.5 seconds in the timeline.

Or alternatively, you can enter a value as string together with "-=" or "+=" before it. This will position the target's animation relative to its default starting point;

```jsx
tl.to("red", {x:200px, duration:2}, "-=0.75")
  .to(".blue", {y:400px, duration:1} "+=0.75");
```

In this case, the "red" target will start 0.75 seconds before its default start time, while the "blue" one will start 0.75 seconds after its default start time.

### See also:

[GSAP Docs](<https://gsap.com/docs/v3/GSAP/gsap.getProperty()>)
[[GreenSock Animation Platform (GSAP) library]]
