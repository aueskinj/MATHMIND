# Logistic Regression

Logistic Regression is a statistical method used for binary classification tasks, where the outcome variable is categorical and has two classes. The logistic regression model applies the logistic function to the linear combination of input features, transforming the result into a probability between 0 and 1. The key components of logistic regression math include the hypothesis function, the cost function, and the process of model training using gradient descent.

### 1. Hypothesis Function:
In logistic regression, the hypothesis function \( h_\theta(x) \) is defined as the logistic or sigmoid function:

\[ h_\theta(x) = \frac{1}{1 + e^{-\theta^Tx}} \]

- \( h_\theta(x) \): Predicted probability that the output is 1 for given input \( x \).
- \( \theta \): Parameters or weights of the model.
- \( x \): Input features.

### 2. Decision Boundary:
The logistic function outputs probabilities between 0 and 1. To make a binary decision, a decision boundary is defined. For example, if \( h_\theta(x) \geq 0.5 \), predict class 1; otherwise, predict class 0.

### 3. Cost Function:
The cost function measures the difference between the predicted probabilities and the actual class labels. The cross-entropy (log loss) cost function for logistic regression is as follows:

\[ J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} \left[ y^{(i)} \log(h_\theta(x^{(i)})) + (1 - y^{(i)}) \log(1 - h_\theta(x^{(i)})) \right] \]

- \( J(\theta) \): Cost function.
- \( m \): Number of training examples.
- \( y^{(i)} \): Actual class label for the \( i \)-th example.
- \( h_\theta(x^{(i)}) \): Predicted probability that \( x^{(i)} \) belongs to class 1.

### 4. Model Training - Gradient Descent:
The goal is to minimize the cost function by adjusting the parameters \( \theta \). Gradient descent is commonly used for this optimization:

\[ \theta_j := \theta_j - \alpha \frac{\partial J(\theta)}{\partial \theta_j} \]

- \( \theta_j \): \( j \)-th parameter.
- \( \alpha \): Learning rate.
- \( \frac{\partial J(\theta)}{\partial \theta_j} \): Partial derivative of the cost function with respect to \( \theta_j \).

This process is iteratively applied until convergence, gradually updating the parameters to find the values that minimize the cost function.
