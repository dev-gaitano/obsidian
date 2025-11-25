---
id: Residual
aliases:
  - Residual
tags:
  - math
  - statistics
  - datascience
  - machinelearning
status: adult
---
---

21:22, Fri 21 November 2025

---

This is the vertical distance between the point of the of the data set and the
fitted line.

![[residual.png]]

It's calculated as follows;

$$
residual = actual data - predicted data
$$

$$
residual_i = y_i - \hat{y}_i
$$

Where $\hat{y}_i = a + bx_i$, therefore

$$
residual_i = y_i - (ax_i + bx)
$$

Where,
$y_i$ = The point of the data set (y-axis)
$a$ = y-intercept
$b$ = Slope
$x_i$ = The point on the data set (x-axis)

### See also:

[[Simple Linear Regression]]

