---
id: GSAP Scroll Trigger
aliases:
  - GSAP Scroll Trigger
tags:
  - gsap
  - libraries
  - webdevelopment
  - react
  - javascript
  - typescript
status: child
---

19:42, Thu 02 October 2025

---

# GSAP Scroll Trigger

The Scroll Trigger is a GSAP plugin that allows the developer to create
animations linked to the page scroll using minimal code.

Using NPM, it's setup like this;

1. Install gsap library using NPM

```sh
npm install gsap
```

2. Import "gsap" and "ScrollTrigger" to your project, unsing an `import` statement.

```js
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
```

3. Register the Scroll Trigger plugin using the `registerPlugin()` gsap method.
   ==Why?==

```js
gsap.registerPlugin(ScrollTrigger);
```

Full setup should should look like this;

```js
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
```

### See also:

[[GSAP Learning - Introducing ScrollTrigger for GSAP]]
[[GSAP Scroll Trigger Usage]]
