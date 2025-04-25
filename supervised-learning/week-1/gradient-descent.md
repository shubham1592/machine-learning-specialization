# Gradient Descent

Gradient Descent is an **optimization algorithm** used to minimize the cost function in machine learning models like linear regression.

---

## Goal
Minimize the cost function `J(θ)` by updating parameters `θ` iteratively.

**Real-life example:** Finding the lowest point in a valley by taking steps downhill, always moving in the direction of steepest descent.

---

## Update Rule
For parameters `θ_j` (where `j = 0, 1`):

`θ_j := θ_j - α * (∂/∂θ_j) J(θ_0, θ_1)`

Where:
- `α`: Learning rate (step size)
- `(∂/∂θ_j) J(θ)`: Partial derivative of cost function

**Real-life example:** Adjusting a recipe iteratively. If a cake is too sweet, you reduce sugar next time. The amount you reduce (learning rate) matters - too little change means slow progress, too much might ruin the cake.

---

## For Linear Regression
The derivatives for univariate linear regression:

`(∂/∂θ_0) J(θ) = (1/m) * Σ(h_θ(x^(i)) - y^(i))`

`(∂/∂θ_1) J(θ) = (1/m) * Σ((h_θ(x^(i)) - y^(i)) * x^(i))`

**Real-life example:** When predicting house prices, if your model consistently predicts $20k too high, you'd adjust your base price down. If you notice you're especially wrong on larger houses, you'd adjust your price-per-square-foot parameter.

---

## Algorithm (Batch Gradient Descent)
Repeat until convergence:
`θ_0 := θ_0 - α * (1/m) * Σ(h_θ(x^(i)) - y^(i))`
`θ_1 := θ_1 - α * (1/m) * Σ(h_θ(x^(i)) - y^(i)) * x^(i)`

**Real-life example:** A delivery company initially estimates 30 minutes base time + 2 minutes per mile for deliveries. After each day, they analyze all deliveries and adjust both numbers based on actual times. If most deliveries were faster than predicted, they might change to 28 minutes + 1.8 minutes per mile.

---

## Key Points
- **Learning rate `α`**: Too small → slow; Too large → may overshoot
- Always move in the direction of **negative gradient**
- Gradient descent can get stuck in **local minima**, though for convex cost functions (like linear regression), global minimum is guaranteed

**Real-life example:** 
- Like adjusting the thermostat: turn it down 1° if too warm (small α) vs. 5° if too warm (large α). The 5° adjustment works faster but might make the room too cold.
- Local minima is like finding the lowest point in your city (which may not be the lowest point in the country). For simple problems like linear regression, there's only one valley, so you'll always find the true lowest point.

---

## Real-Life Analogy
- Like descending a mountain in foggy conditions using only local slope info
- Imagine being on a mountain with a foggy view. You can only see a few feet around you:
  - You feel the ground in all directions to determine the steepest downhill path
  - Take a step in that direction
  - Repeat until you're no longer going downhill

---

## Types of Gradient Descent
- **Batch Gradient Descent**: All training examples used in each update
  - Example: A restaurant changes its menu after collecting feedback from all customers over a month
- **Stochastic Gradient Descent (SGD)**: One example used per update
  - Example: Adjusting your cooking immediately after each person tastes and comments
- **Mini-batch Gradient Descent**: Subset (mini-batch) used per update
  - Example: A teacher modifying lesson plans after getting feedback from groups of 5 students at a time

---

## Applications
- Training ML models (linear regression, logistic regression, neural networks)
- Optimization problems in economics, finance, engineering
- **Specific example**: A solar panel company uses gradient descent to find the optimal angle for panels based on location data
- **Specific example**: Online retailers optimize prices daily by analyzing how small price changes affect purchase volumes

---

## Example
Suppose you start with `θ_0 = 0, θ_1 = 0`, learning rate `α = 0.01`
Each step moves `θ_0, θ_1` closer to the values that minimize `J(θ)`

**Concrete example**: A coffee shop predicts sales based on temperature. They start with the formula `sales = 0 + 0*temperature` (essentially guessing zero sales regardless of temperature). After the first round of gradient descent with real data, they might update to `sales = 100 + 5*temperature`. After several more iterations, they might reach `sales = 200 + 12*temperature`, meaning they expect 200 cups on a 0° day and 12 more cups for each degree increase.

Monitor convergence by plotting `J(θ)` over iterations.