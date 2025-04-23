# Machine Learning: Core Concepts and Models

## Types of Machine Learning

### 1. Supervised Learning
Learns from labeled data — input \( x \) maps to output \( y \).

- **Goal**: Learn a function that approximates the mapping from inputs to outputs.
- **Example**: Email spam classification (Spam = 1, Not Spam = 0)
- **Applications**: Fraud detection, sentiment analysis, disease prediction.

### 2. Unsupervised Learning
Finds structure in data without labels.

- **Clustering**: e.g., Customer segmentation.
- **Anomaly Detection**: e.g., Fraud detection.
- **Dimensionality Reduction**: e.g., PCA for data compression.

### 3. Reinforcement Learning
Learns by interacting with an environment to maximize cumulative reward.

- **Example**: AlphaGo, Self-driving car navigation.
- **Applications**: Robotics, game AI, trading algorithms.

---

## Supervised Learning: Linear Regression (Single Variable)

### Model
\[
f_{w,b}(x) = wx + b
\]

### Parameters
- \( w \): weight (slope)
- \( b \): bias (intercept)

### Cost Function
\[
J(w, b) = \frac{1}{2m} \sum_{i=1}^{m} \left( f_{w,b}(x^{(i)}) - y^{(i)} \right)^2
\]

Where:
- \( m \): number of training examples
- \( x^{(i)} \): i-th input
- \( y^{(i)} \): i-th true output
- \( f_{w,b}(x^{(i)}) \): predicted output

### Objective
\[
\min_{w,b} J(w, b)
\]

### Applications
- Predicting house prices based on size
- Forecasting stock prices (linear trend)
- Estimating sales based on advertising spend

---

## Note
- Linear regression assumes a linear relationship between input and output.
- Cost function is MSE (Mean Squared Error), differentiable, convex.
- Gradient Descent is used to minimize cost and update \( w \) and \( b \).
