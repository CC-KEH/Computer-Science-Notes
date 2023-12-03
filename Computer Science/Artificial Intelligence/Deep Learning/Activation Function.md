# Activation Function

### Sigmoid Function

- **Formula:** σ(x)=1/(1+e−x1)
- **Range:** (0, 1)
- **Properties:**
  - Smooth gradient, facilitating efficient backpropagation.
  - Output interpreted as probabilities in binary classification.

### Hyperbolic Tangent (tanh) Function

- **Formula:** tanh(x)=e2x−1​/e2x+1
- **Range:** (-1, 1)
- **Properties:**
  - Similar to the sigmoid but with an output range from -1 to 1.
  - Zero-centered, which can speed up learning in certain cases.

### Rectified Linear Unit (ReLU)

- **Formula:** f(x)=max(0,x)
- **Range:** \((0, \infty)\)
- **Properties:**
  - Simple and computationally efficient.
  - Addresses the vanishing gradient problem.

### Leaky Rectified Linear Unit (Leaky ReLU)

- **Formula:** f(x)=max(αx,x) where α is a small positive constant.
- **Range:** \((-\infty, \infty)\)
- **Properties:**
  - Addresses the "dying ReLU" problem by allowing a small gradient when \(x < 0\).

### Softmax Function

- **Formula:** Softmax(xi​)=exi /∑j exj
- **Output:** Converts a vector of real numbers into a probability distribution.
- **Application:** Commonly used in the output layer of a neural network for multi-class classification problems.

## Importance of Activation Functions

- **Non-Linearity:** Activation functions introduce non-linearity, enabling neural networks to learn complex patterns and relationships in data.
- **Gradient Flow:** Non-linear activation functions allow for effective backpropagation of errors during training.
- **Diversity:** Different activation functions serve various purposes and are suitable for different types of problems. Choosing the right activation function can significantly impact the performance of a neural network.
