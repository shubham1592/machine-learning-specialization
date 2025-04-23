# Gradient Descent

Gradient Descent is an **optimization algorithm** used to minimize the cost function in machine learning models like linear regression.

---

## Goal
Minimize the cost function \( J(\theta) \) by updating parameters \( \theta \) iteratively.

---

## Update Rule
For parameters \( \theta_j \) (where \( j = 0, 1 \)):

\[ \theta_j := \theta_j - \alpha \frac{\partial}{\partial \theta_j} J(\theta_0, \theta_1) \]

Where:
- \( \alpha \): Learning rate (step size)
- \( \frac{\partial}{\partial \theta_j} J(\theta) \): Partial derivative of cost function

---

## For Linear Regression
The derivatives for univariate linear regression:

\[ \frac{\partial}{\partial \theta_0} J(\theta) = \frac{1}{m} \sum_{i=1}^{m}(h_\theta(x^{(i)}) - y^{(i)}) \]

\[ \frac{\partial}{\partial \theta_1} J(\theta) = \frac{1}{m} \sum_{i=1}^{m}((h_\theta(x^{(i)}) - y^{(i)})x^{(i)}) \]

---

## Algorithm (Batch Gradient Descent)
Repeat until convergence:
\[ \theta_0 := \theta_0 - \alpha \cdot \frac{1}{m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)}) \]
\[ \theta_1 := \theta_1 - \alpha \cdot \frac{1}{m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)}) x^{(i)} \]

---

## Key Points
- **Learning rate \( \alpha \)**: Too small → slow; Too large → may overshoot
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
Suppose you start with \( \theta_0 = 0, \theta_1 = 0 \), learning rate \( \alpha = 0.01 \)
Each step moves \( \theta_0, \theta_1 \) closer to the values that minimize \( J(\theta) \)

Monitor convergence by plotting \( J(\theta) \) over iterations.

