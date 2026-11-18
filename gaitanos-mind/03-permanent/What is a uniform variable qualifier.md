---
id: What is a uniform variable qualifier
aliases:
- Uniform
- uniforms
- uniform variables
tags:
- shaders
- glsl
status: adult
---

---

14:42, Sun 15 November 2026

---

A uniform is a [[variable qualifier]].

Uniform [[Variable|variables]] contain read-only data that is sent from the CPU to to the fragment or
vertex shader. This input is equal in all threads, hence the name "uniform".

For example, screen resolution, time since the shader started and mouse position.

Uniform variables come in most of the supported types: [[Vector|vectors]], [[What is a Matrix|matrices]] and [[samplers]].

Uniforms have multiple naming conventions, one naming convention is putting "u_"
before the variable name.

Examples of uniforms in practice:

```glsl
// uniform type u_variable_name
uniform vec2 u_resolution;  // Canvas size (width,height)
uniform vec2 u_mouse;       // mouse position in screen pixels
uniform float u_time;       // Time in seconds since load
```

### See also:

[Book of shaders - 03 - Uniforms](https://thebookofshaders.com/03/)
[[What is an attribute variable qualifier]]
[[What is a varying variable qualifier]]
