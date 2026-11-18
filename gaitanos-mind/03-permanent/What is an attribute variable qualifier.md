---
id: What is an attribute variable qualifier
aliases:
- attribute
- attributes
- attribute variable
tags:
- shaders
- glsl
status: adult
---

---

16:08, Sun 15 November 2026

---

An attribute is a [[variable qualifier]].

Attribute [[Variable|variables]] contain read-only data that is sent from the CPU to the vertex shader.

This data is specific to each vertex since the vertex shader is executed once
for each vertex.

For example vertex position and color. These values needs to be specific to each
vertex because vertices don't all share the same position or color.

Attribute variables come in most of the supported types: [[Vector|vectors]], [[What is a Matrix|matrices]] and [[samplers]].

Attributes have multiple naming conventions, one naming convention is putting "a_"
before the variable name.

An example of an attribute in practice:

```glsl
attribute vec3 a_position;
```

### See also:

[Book of shaders - Attributes](https://thebookofshaders.com/glossary/?search=attribute)
[[What is a uniform variable qualifier]]
[[What is a varying variable qualifier]]
