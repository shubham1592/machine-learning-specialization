# Linear Regression Model

Linear regression is a supervised learning algorithm used for **predicting a continuous value** given a set of input features. It models the relationship between the input variable(s) `x` and the output variable `y` using a linear function.

---

## Hypothesis Representation

We try to approximate the target function with:

$$h_\theta(x) = \theta_0 + \theta_1x$$

Where:
- $h_\theta(x)$: Hypothesis (predicted output)
- $\theta_0$: Intercept (bias term)
- $\theta_1$: Slope (weight or coefficient of input)
- $x$: Input feature

This is a **univariate linear regression** (one feature).

---

## Cost Function (J)

The cost function measures how well our hypothesis matches the data:

$$J(\theta_0, \theta_1) = \frac{1}{2m} \sum_{i=1}^m \left(h_\theta(x^{(i)}) - y^{(i)}\right)^2$$

Where:
- $m$: Number of training examples
- $x^{(i)}, y^{(i)}$: The i-th training example
- This is called the **Mean Squared Error (MSE)** cost function.

---

## Objective

Minimize the cost function $J(\theta_0, \theta_1)$ by finding optimal values of $\theta_0$ and $\theta_1$.

---

## Assumptions in Linear Regression
- Linearity of relationship between inputs and output
- Independence of errors
- Homoscedasticity (constant variance of errors)
- Normal distribution of errors (for inference)

---

## Real-Life Applications
- Predicting housing prices based on area, number of rooms, etc.
- Estimating salary based on experience and education
- Forecasting sales based on past data

---

## Example
Given data:

| Experience (Years) | Salary (k$) |
|-------------------|-------------|
| 1                 | 40          |
| 2                 | 45          |
| 3                 | 50          |

Fitting linear regression gives:
$$h_\theta(x) = 35 + 5x$$
Meaning:
- For each year of experience, salary increases by 5k$
- A fresher (0 years) is expected to earn 35k$

---

## Visualization
A line of best fit that minimizes the squared errors from each data point to the line.

$$\text{minimize } \sum (y_i - h_\theta(x_i))^2$$

---

Linear regression serves as the foundation for more complex models like **polynomial regression** and **logistic regression**.