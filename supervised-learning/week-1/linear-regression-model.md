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

**Real-life example:** Imagine predicting a child's height (`y`) based on their age (`x`). The formula might be `height = 80 + 5*age`, meaning a newborn is 80cm and grows 5cm each year.

---

## Cost Function (J)

The cost function measures how well our hypothesis matches the data:

`J(θ_0, θ_1) = (1/2m) * Σ(h_θ(x^(i)) - y^(i))²`

Where:
- `m`: Number of training examples
- `x^(i), y^(i)`: The i-th training example
- This is called the **Mean Squared Error (MSE)** cost function.

**Real-life example:** When fitting a linear regression to housing prices, this would be like measuring the average squared difference between your predicted prices and actual sale prices. If houses sold for $350k, $420k, and $390k, but your model predicted $330k, $450k, and $380k, your errors would be $20k, $30k, and $10k, producing an MSE of (400 + 900 + 100)/3 = $466.67 million (squared dollars).

---

## Objective

Minimize the cost function `J(θ_0, θ_1)` by finding optimal values of `θ_0` and `θ_1`.

**Real-life example:** A retail store wants to predict daily sales based on outdoor temperature. Finding the optimal parameters means finding the line that best describes how sales increase with temperature, minimizing prediction errors.

---

## Assumptions in Linear Regression
- Linearity of relationship between inputs and output
- Independence of errors
- Homoscedasticity (constant variance of errors)
- Normal distribution of errors (for inference)

**Real-life example:** When predicting ice cream sales based on temperature, we assume:
- Each 1°F increase causes roughly the same increase in sales (linearity)
- Error in Monday's prediction doesn't affect Tuesday's error (independence)
- Prediction errors are similar in magnitude whether it's hot or cold (homoscedasticity)
- Errors follow a bell curve distribution (normality)

---

## Real-Life Applications
- **Housing market**: Predicting house prices based on square footage, bedrooms, location scores
  - Example: A model finds that each additional square foot adds $120 to home value
- **Healthcare**: Predicting patient hospital stay duration based on age, severity scores
  - Example: Each point on the severity scale adds 0.8 days to expected stay
- **Finance**: Forecasting stock prices based on economic indicators
  - Example: Each 0.1% interest rate increase correlates with a 2.5% market decline
- **Agriculture**: Predicting crop yield based on rainfall, temperature, fertilizer
  - Example: Each inch of rainfall increases corn yield by 1.8 bushels/acre

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

**Extended example:** A tech company collected salary data from 50 employees and found the relationship `salary = 35 + 5*experience + 2*certifications + 7*education_level`. This means someone with 4 years experience, 3 certifications, and a Master's degree (education_level = 2) would expect: $35k + $20k + $6k + $14k = $75k salary.

---

## Visualization
A line of best fit that minimizes the squared errors from each data point to the line.

`minimize Σ(y_i - h_θ(x_i))²`

**Real-life example:** Imagine fitting a trend line through a city's monthly temperature readings. The best line passes close to most points, with some slightly above and some below. This line can predict future temperatures based on the month.

---

## Common Issues and Solutions
- **Outliers**: A single house selling for 10x market rate can skew results
  - Solution: Remove outliers or use robust regression methods
- **Multicollinearity**: When house bedrooms and square footage are highly correlated
  - Solution: Feature selection or dimensionality reduction
- **Overfitting**: Creating a complex model that fits training data perfectly but fails on new data
  - Solution: Regularization techniques (Ridge, Lasso)

---

Linear regression serves as the foundation for more complex models like **polynomial regression** and **logistic regression**.