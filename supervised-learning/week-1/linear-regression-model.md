# Linear Regression Model

Linear regression is a supervised learning algorithm used for **predicting a continuous value** given a set of input features. It models the relationship between the input variable(s) `x` and the output variable `y` using a linear function.

---

## Hypothesis Representation

We try to approximate the target function with:

`h_θ(x) = θ_0 + θ_1*x`

Where:
- `h_θ(x)`: Hypothesis (predicted output)
- `θ_0`: Intercept (bias term)
- `θ_1`: Slope (weight or coefficient of input)
- `x`: Input feature

This is a **univariate linear regression** (one feature).

---

## Cost Function (J)

The cost function measures how well our hypothesis matches the data:

`J(θ_0, θ_1) = (1/2m) * Σ(h_θ(x^(i)) - y^(i))²`

Where:
- `m`: Number of training examples
- `x^(i), y^(i)`: The i-th training example
- This is called the **Mean Squared Error (MSE)** cost function.

---

## Objective

Minimize the cost function `J(θ_0, θ_1)` by finding optimal values of `θ_0` and `θ_1`.

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
`h_θ(x) = 35 + 5x`
Meaning:
- For each year of experience, salary increases by 5k$
- A fresher (0 years) is expected to earn 35k$

---

## Visualization
A line of best fit that minimizes the squared errors from each data point to the line.

`minimize Σ(y_i - h_θ(x_i))²`

---

Linear regression serves as the foundation for more complex models like **polynomial regression** and **logistic regression**.