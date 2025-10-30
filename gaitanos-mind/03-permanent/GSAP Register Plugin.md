---
id: GSAP Register Plugin
aliases:
  - GSAP Register Plugin
tags:
  - gsap
  - gsap-plugins
  - libraries
  - webdevelopment
  - javascript
  - typescript
status: child
---

13:16, Thu 09 October 2025

---

# GSAP Register Plugin

```jsx
gsap.registerPlugin();
```

The `.registerPlugin()` is a GSAP method that takes in [[GSAP Plugins]] as
arguments.

Registering a Plugin allows GSAP's core to work seamlessly with the plugins by making it
more aware of the individual plugins and also prevents Tree Shaking by build
tools and/or bunders.

You only need to register a plugin once before using it.

You can pass in as many plugins as possible as arguments in the
`.registerPlugin()` method separated my commas, like this;

```jsx
gsap.registerPlugin(ScrollTrigger, MotionPathPlugin, TextPlugin);
```

**NB:This is not a replacement for importing GSAP plugins**

### See also:

[[GreenSock Animation Platform (GSAP) library]]
