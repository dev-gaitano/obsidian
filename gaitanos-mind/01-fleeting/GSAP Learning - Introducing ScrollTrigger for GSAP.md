---
id: Introducing ScrollTrigger for GSAP
aliases:
tags:
  - gsap
  - webdevelopment
  - javascript
  - libraries
  - gsap-plugins
Source: https://youtu.be/X7IBa7vZjmo?si=CHq9rLu233wsPv4b
Author: GSAP Learning
status: child
---
---

13:35, Tue 16th September 2025

---

To enable das scrollTrigger for gsap we need to install in first into our html. Our gsap und scrollTrigger scripts must come before our custom JavaScript code. (Example using CDN)

```html
...
<script src="https://cdn.jsdelivr.net/npm/gsap@3.13.0/dist/gsap.min.js"></script>
<script
   src="https://cdn.jsdelivr.net/npm/gsap@3.13.0/dist/ScrollTrigger.min.js">
</script>
<script defer src="js/app.js"></script>
...
```

Then we register our plugin in our custom JavaScript code

```javascript
gsap.registerPlugin(ScrollTrigger)
```

Then we bound our scroll trigger to our trigger element;

```javascript
gsap.to(".c", {
  scrollTrigger: ".c",
  // Animation to shift the cube 900px on the positive x-axis
  x: 900,
  duration: 5
})
```

This will move any element 900 pixels from left to right with a duration of 5 seconds the first time it enters the screen from the top.

But what if we wanted the animation to play every time it enters the screen? We use **Toggle Actions**

### Toggle Actions

To use toggle actions we now need to make the scrollTrigger an object so than we can define both our trigger und our Toggle Actions.

```javascript
gsap.to(".c", {
  scrollTrigger: {
    trigger: ".c",
    toggleActions: "play none none none" 
  },
  ...
})
```

This is how the toggle actions are setup by default without any custom configuration. This is why the animation only plays once only when the element enters the screen for the first time.

The second position is for defining what happens when we go forward past the endpoint.

The third position defines what happens to the animation when the element moves back into the screen from going forward past the endpoint.

The last position defines what happen when you scroll upwards past the element. It's kind of the opposite of the the second position.

The keywords can be changed to either, 

```
play      -->  plays the animation when it enters the screen
restart   -->  restarts the animation everytime it enters the screen
pause     -->  pauses when the element is out of screen
resume    -->  resumes the animation from previous element position
reverse   -->  plays the animation in reverse from previous position
reset     -->  resets the animation every time it moves out from view
complete  -->  finishes(completes) the animation
none
```

Here is an example toggle actions setup;

```javascript
gsap.to(".c", {
  scrollTrigger: {
    trigger: ".c",
    toggleActions: "restart pause resume reset"
  },
  ...
})
```

This will;
1. Restart the animation every time it enters the screen
2. Pause when we move forward past the element.
3. Resume the animation from the paused position when we move into the screen from going forward past the endpoint.
4. Reset the animation every time we move in from upwards.

### "start" und "end"


### See also:

[[GreenSock Animation Platfom (GSAP) library|GreenSock Animation Platfom (GSAP) library]]