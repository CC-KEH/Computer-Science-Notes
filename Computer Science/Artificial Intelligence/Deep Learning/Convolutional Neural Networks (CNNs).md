## Introduction
Convolutional Neural Networks (CNNs) are a class of deep neural networks designed for processing structured grid data, such as images. CNNs have proven highly effective in computer vision tasks, demonstrating superior performance in tasks like image classification, object detection, and image segmentation.

![[Pasted image 20231202150425.png]]

## Basic Architecture
### Convolutional Layers
- **Convolution Operation:**
  - Applies convolutional filters (kernels) to input images.
  - Example: Detecting edges using a convolutional filter like the Sobel operator.

- **Striding:**
  - Determines the step size of the convolutional filter as it moves across the input.
  - Example: A stride of 2 reduces the spatial dimensions of the feature maps.

- **Padding:**
  - Adding border pixels to the input to preserve spatial information during convolution.
  - Example: "Same" padding ensures the output size matches the input size.

### Activation Function
- **Rectified Linear Unit (ReLU):**
  - Commonly used activation function in CNNs.
  - f(x) = max(0, x)
  - Example: Introduces non-linearity, allowing the network to learn complex patterns.

### Pooling Layers
- **Max Pooling:**
  - Downsampling technique, selecting the maximum value from a region.
  - Example: Reducing the spatial resolution of feature maps.

- **Average Pooling:**
  - Takes the average value from a region for downsampling.
  - Example: Further reducing the dimensionality while preserving important information.

## Advanced Techniques
### Batch Normalization
- **Idea:**
  - Normalizes input to each layer, improving convergence and reducing internal covariate shift.
  - Example: Stabilizes training by normalizing activations within each mini-batch.

### Dropout
- **Idea:**
  - Randomly drops a fraction of neurons during training to prevent overfitting.
  - Example: Regularizes the network, improving generalization.

### Skip Connections (Residual Networks)
- **Idea:**
  - Introduces shortcut connections, allowing the network to learn residual functions.
  - Example: Residual blocks facilitate the training of very deep networks.

### Dilated (Atrous) Convolution
- **Idea:**
  - Increases the receptive field without increasing the number of parameters.
  - Example: Used in semantic segmentation to capture contextual information.

## Working of CNNs - Example

### Input Layer
- **Input:**
  - RGB image (e.g., 224x224 pixels).

### Convolutional and Activation Layers
- **Conv1:**
  - Applies multiple filters to detect simple features (edges, textures).
  - Activation: ReLU.

- **Conv2:**
  - Captures more complex features using deeper filters.
  - Activation: ReLU.

### Pooling Layer
- **Max Pooling:**
  - Reduces spatial dimensions while retaining important features.

### Fully Connected Layers
- **Flattening:**
  - Reshapes the 3D feature maps into a 1D vector.
  
- **Dense Layers:**
  - Capture high-level abstractions and perform the final classification.

### Output Layer
- **Softmax Activation:**
  - Converts the network's output into probability scores for each class.

### Training
- **Loss Function:**
  - Typically cross-entropy for classification tasks.

- **Backpropagation:**
  - Adjusts weights and biases through optimization algorithms (e.g., SGD, Adam).

### Inference
- **Prediction:**
  - The trained model is used to make predictions on new, unseen data.


![[Pasted image 20231203130000.png]]
![[Pasted image 20231203130434.png]]



# Questions
![[Pasted image 20231203131123.png]]

## Solution
![[Pasted image 20231203131135.png]]
![[Pasted image 20231203131145.png]]
![[Pasted image 20231203131155.png]]
![[Pasted image 20231203131202.png]]
![[Pasted image 20231203131209.png]]



# Visualizations
[Interactive Tool](https://poloclub.github.io/cnn-explainer/)
