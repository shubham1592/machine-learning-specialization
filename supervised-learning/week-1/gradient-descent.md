# Gradient Descent

Gradient Descent is an **optimization algorithm** used to minimize the cost function in machine learning models like linear regression.

---

## Goal
Minimize the cost function `J(θ)` by updating parameters `θ` iteratively.

---

## Update Rule
For parameters `θ_j` (where `j = 0, 1`):

`θ_j := θ_j - α * (∂/∂θ_j) J(θ_0, θ_1)`

Where:
- `α`: Learning rate (step size)
- `(∂/∂θ_j) J(θ)`: Partial derivative of cost function

---

## For Linear Regression
The derivatives for univariate linear regression:

`(∂/∂θ_0) J(θ) = (1/m) * Σ(h_θ(x^(i)) - y^(i))`

`(∂/∂θ_1) J(θ) = (1/m) * Σ((h_θ(x^(i)) - y^(i)) * x^(i))`

---

## Algorithm (Batch Gradient Descent)
Repeat until convergence:
`θ_0 := θ_0 - α * (1/m) * Σ(h_θ(x^(i)) - y^(i))`
`θ_1 := θ_1 - α * (1/m) * Σ(h_θ(x^(i)) - y^(i)) * x^(i)`

---

## Key Points
- **Learning rate `α`**: Too small → slow; Too large → may overshoot
- Always move in the direction of **negative gradient**
- Gradient descent can get stuck in **local minima**, though for convex cost functions (like linear regression), global minimum is guaranteed

---

## Real-Life Analogy
- Like going downhill in foggy mountains using only local slope info

---

## Types of Gradient Descent
- **Batch Gradient Descent**: All training examples used in each update
- **Stochastic Gradient Descent (SGD)**: One example used per update
- **Mini-batch Gradient Descent**: Subset (mini-batch) used per update

---

## Applications
- Training ML models (linear regression, logistic regression, neural networks)
- Optimization problems in economics, finance, engineering

---

## Example
Suppose you start with `θ_0 = 0, θ_1 = 0`, learning rate `α = 0.01`
Each step moves `θ_0, θ_1` closer to the values that minimize `J(θ)`

Monitor convergence by plotting `J(θ)` over the iterations.