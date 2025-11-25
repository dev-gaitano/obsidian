---
id: Linear Regression
aliases:
  - Linear Regression
tags:
  - math
  - statistics
  - datascience
  - machinelearning
status: child
---
---

17:02, Fri 21 November 2025

---

The Linear regression model, also known as Ordinary Least Squares(OLS) regression model,
is a model that estimates the relationship between a value you want to predict,
known as a [[Dependent Variable|Dependent variable]] and one or more "things" that influence the value
you want to predict, known as explanatory variables or [[Independent Variable|Independent variables]].

The relationships are modeled using a math function(==linear Predictor Function==)
whose unknown parameters are estimated from the data.

$$
y_i = ax_i + b + e_i
$$

$y$ = Dependent variable
$a$ = Slope/gradient
$b$ = y-intercept
$e$ = values that may affect "y" but aren't observed (errors)
$i$ = 1, ..., n

This formula allows one to plot a line that minimizes the sum of squared
[[Residual|residuals]], also known as the [[Mean Squared Error]](MSE). Hence the name
OLS regression model.

The [[Gradient Descent|Gradient descent]] method can then be used to further minimize
MSE by finding the optimal Slope and Intercept by checking how the MSE changes
with each parameter, then moving in the direction that reduces MSE.

The quality of the fitting can be measured using the [[Coefficient of Determination]]($R^2$).

A model with only one explanatory variable is referred to as [[Simple Linear Regression]],
while a model with two or more explanatory variables is known as Multiple Linear Regression.

![[Linear_regression.png]]

### See also:

[Wikipedia | Linear regression](https://en.wikipedia.org/wiki/Linear_regression)
