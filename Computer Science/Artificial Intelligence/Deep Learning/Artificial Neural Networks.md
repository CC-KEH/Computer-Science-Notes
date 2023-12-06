# Neural Networks

## Definition
Neural networks are a class of machine learning models inspired by the structure and functioning of the human brain. They consist of interconnected nodes, known as neurons, organized into layers. Neural networks are capable of learning complex patterns and representations from data.

## Basic Components
### Neurons
- **Neurons (Nodes):** The basic computational units that receive input, apply a transformation using weights and biases, and produce an output.
- **[[Activation Function]]:** Determines the output of a neuron based on its input. Common activation functions include sigmoid, tanh, and rectified linear unit (ReLU).

### Layers
- **Input Layer:** Receives the initial input data.
- **Hidden Layers:** Intermediate layers between the input and output layers, where complex representations are learned.
- **Output Layer:** Produces the final output.

### Weights and Biases
- **Weights:** Parameters that the model learns during training to adjust the strength of connections between neurons.
- **Biases:** Offsets that allow the model to represent patterns even when all inputs are zero.

## Some Common Architecture Types
- **[[McCulloch-Pitts Neuron (MP)]]**
- **[[Rosenblatt Neuron (Perceptron)]]**
- **[[Feedforward Neural Networks (FNN)]]**
- **[[Recurrent Neural Networks (RNN)]]**
- **[[Convolutional Neural Networks (CNN)]]**
- **[[Long Short-Term Memory (LSTM)]] and [[Gated Recurrent Unit (GRU)]]**
- **[[Transformers]]**



## Training Process
### [[Backpropagation]]
- Optimization algorithm used to minimize the error between predicted and actual outputs.
- Involves calculating gradients and adjusting weights and biases accordingly.

### Loss Functions
- Measure the difference between predicted and true values. Common losses include Mean Squared Error (MSE) for regression and Cross-Entropy for classification.

### Optimization Algorithms
- **Gradient Descent:** Update weights in the opposite direction of the gradient.
- **Adam, RMSProp, SGD:** Variations of gradient descent with adaptive learning rates.

