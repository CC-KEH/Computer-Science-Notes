# Activation Function

# Types of Activation Functions

## 1. Linear Functions
   - **Definition:** \(f(x) = ax + b\), where \(a\) and \(b\) are constants.
## 2. Step Functions
   - **Definition:** A function that has a constant value within specific intervals and changes its value abruptly at the boundaries of these intervals.
### Binary Step Function
![[Pasted image 20231206161746.png]]

### Bipolar Step Function
![[Pasted image 20231206161826.png]]

## 3. Non-linear Functions
   - **Definition:** Any function that is not a linear function. It can have curves, bends, or other complex shapes when graphed.
### Sigmoid Function
- **Formula:** σ(x)=1/(1+e−x1)
- **Range:** (0, 1)
- **Properties:**
  - Smooth gradient, facilitating efficient backpropagation.
  - Output interpreted as probabilities in binary classification.

### Binary Sigmoid Function
![[Pasted image 20231206162406.png]]

### Bipolar Sigmoid Function
![[Pasted image 20231206162630.png]]
### Hyperbolic Tangent (tanh) Function
![[Pasted image 20231206163826.png]]
### Rectified Linear Unit (ReLU)
![[Pasted image 20231206163953.png]]
### Leaky Rectified Linear Unit (Leaky ReLU)
![[Pasted image 20231206164114.png]]
### Softmax Function
![[Pasted image 20231206164202.png]]
## Importance of Activation Functions
- **Non-Linearity:** Activation functions introduce non-linearity, enabling neural networks to learn complex patterns and relationships in data.
- **Gradient Flow:** Non-linear activation functions allow for effective backpropagation of errors during training.
- **Diversity:** Different activation functions serve various purposes and are suitable for different types of problems. Choosing the right activation function can significantly impact the performance of a neural network.
