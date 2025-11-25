---
id: GreenSock Animation Platfom (GSAP) library
aliases:
  - GreenSock Animation Platfom (GSAP) library
tags:
  - gsap
  - libraries
  - webdevelopment
  - javascript
  - typescript
status: adult
---

14:10, Thu 09 October 2025

---

GSAP is a framework-agnostic [[JavaScript]] library that simplifies the process of
creating web animations. ([[Libraries]])

It can be installed through;

1. CDN

```html
<script src="https://cdn.jsdelivr.net/npm/gsap@3.13/dist/gsap.min.js"></script>
```

2. NPM

```sh
npm install gsap
```

```jsx
import { gsap } from "gsap";
```

To use GSAP, we have to use the `gsap` object in our code. It's a regular object
with methods and acts as an access point to the GSAP engine.

These methods have properties that create and control "Tweens" [[GSAP Tweens]] and "Timelines" [[GSAP Timelines]] -
Two very important concepts to understand.

**NB: GSAP offers a wide variety of plugins that enhance it's functionality and
compatibility with other libraries.** [[GSAP Plugins]]

### See also:

[GSAP NPMJS](https://www.npmjs.com/package/gsap)
[GSAP Docs](https://gsap.com/docs/v3/GSAP/)
