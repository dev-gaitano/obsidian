---
id: What is a varying variable qualifier
aliases:
- varying
- varying variable
tags:
- shaders
- glsl
status: adult
---

---

13:37, Wed 18 November 2026

---

A varying is a [[variable qualifier]].

Varyng [[Variable|variables]] contain data that is shared from a vertex shader to a fragment shader.

This variable s defined in the vertex shader and the value is passed as
read-only to the fragment shader.

Varying variables come in most of the supported types: [[Vector|vectors]], [[What is a Matrix|matrices]] and [[samplers]].

An example of a varying in practice:

```glsl
varying vec3 position;
```

### See also:

[Book of shaders - Varying](https://thebookofshaders.com/glossary/?search=varying)
[[What is a uniform variable qualifier]]
[[What is an attribute variable qualifier]]
