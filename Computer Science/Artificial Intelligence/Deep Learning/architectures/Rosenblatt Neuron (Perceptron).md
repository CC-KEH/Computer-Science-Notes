# Definition
- Frank Rosenblatt, an American psychologist, proposed the classical perceptron model in 1958. Further refined and carefully analyzed by Minsky and Papert (1969) their model is referred to as the perceptron model.
- It follows Supervised Learning
- Inputs are no longer limited to boolean values like in the case of an M-P neuron, it supports real inputs as well which makes it more useful and generalized.
- Perceptron also work on problems they are linearly separable.
- The perceptron is also called as Rosenblatt neuron.

# Architecture & Working
![[Pasted image 20231206165941.png]]


## Training
![[Pasted image 20231206170040.png]]
![[Pasted image 20231206170254.png]]
![[Pasted image 20231206170307.png]]


## Testing
![[Pasted image 20231206170524.png]]





# Limitations of Perceptron
- Although it was said the Perceptron could represent any circuit and logic, the biggest criticism was that it couldn’t represent the XOR gate, exclusive OR, where the gate only returns 1 if the inputs are different.

- This was proved almost a decade later by Minsky and Papert, in 1969 and highlights the fact that Perceptron, with only one neuron, can’t be applied to non-linear data.

- The Multilayer Perceptron was developed to tackle this limitation of Perceptron. It is a neural network where the mapping between inputs and output is non-linear.

- A Multilayer Perceptron has input and output layers, and one or more hidden layers with many neurons stacked together.

- And while in the Perceptron the neuron must have an activation function that imposes a threshold, like ReLU or sigmoid, neurons in a Multilayer Perceptron can use any arbitrary activation function.

- Multilayer Perceptron falls under the category of **feedforward algorithms**, because inputs are combined with the initial weights in a weighted sum and subjected to the activation function, just like in the Perceptron. But the difference is that each linear combination is propagated to the next layer.

- Each layer is feeding the next one with the result of their computation, their internal representation of the data. This goes all the way through the hidden layers to the output layer.

- If the algorithm only computed the weighted sums in each neuron, propagated results to the output layer, and stopped there, it wouldn’t be able to learn the weights that minimize the cost function. If the algorithm only computed one iteration, there would be no actual learning.

- This is where [[Backpropagation]] comes into play.



