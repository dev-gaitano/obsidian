---
id: 
aliases: 
tags: 
Source: 
Author: 
status:
---
---

15:08, Thu 24th July 2025

---

Use Effect's callback function cannot be an async function, so if you need an async function you have to define another function inside of the callback, for example;

```tsx
// This is Right!
useEffect(() => {
	const someFunction = async () => {
		...
	}
})
```

Not;

```tsx
// This is wrong
useEffect(async() => {
	...
})
```

### See also: