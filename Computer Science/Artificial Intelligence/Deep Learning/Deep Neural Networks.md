# Deep Neural Networks

# Transfer Learning
Transfer learning is a machine learning technique where a model trained on one task is adapted to work on a second related task. In the context of deep learning, transfer learning involves using pre-trained neural network models as a starting point for a new task. Instead of training a deep neural network from scratch, transfer learning leverages the knowledge gained from solving one problem and applies it to a different, but related, problem.

The main idea behind transfer learning is that features learned by a model on a large dataset and complex task can be useful for a different task. There are two common scenarios in transfer learning:

1. **Feature Extraction:**
   - Use the pre-trained model as a fixed feature extractor.
   - Remove the final layers of the pre-trained model.
   - Add new layers to the model for the specific task and train only these new layers.
   - Well-known architectures for feature extraction include VGG, ResNet, and Inception.

   **Example:**
   - Take a pre-trained image classification model, remove the final classification layer, and add a new layer for a specific classification task (e.g., distinguishing between cats and dogs).

2. **Fine-Tuning:**
   - Use the pre-trained model as the initial weights.
   - Retrain the entire model on the new task with a smaller learning rate.
   - Allows the model to adjust its parameters to the specifics of the new task.

   **Example:**
   - Use a pre-trained language model (e.g., BERT) and fine-tune it on a specific natural language processing task, like sentiment analysis.

**Benefits of Transfer Learning:**

- **Reduced Training Time:** Since the model starts with pre-learned features, it often converges faster on the new task.
  
- **Requires Less Data:** Transfer learning is effective even when the new task has limited labeled data.

- **Improved Generalization:** The knowledge gained from a source task can help the model generalize better to the target task.


# Some Famous Transfer Learning Models
## LeNet-5s
- Classic convolutional neural network employing the use of convolutions, pooling and fully connected layers.
- Was used in detecting handwritten cheques by banks based on MNIST dataset (10 Classes).
- LeNet-5 introduced convolutional and pooling layers.
- LeNet-5 is believed to be the base for all other ConvNets.
- A convolution is a linear operation.
- The convolutional layer does the major job by multiplying weight (kernel/filter) with the input.
- A pooling layer generally comes after a convolutional layer. This layer helps in reducing the high dimensionality created by convolutional layers, to curb overfitting.

### Architecture
![[Pasted image 20231203133330.png]]
The network has **5 layers** with learnable parameters and hence named Lenet-5. It has
three sets of convolution layers with a combination of average pooling. After the
convolution and average pooling layers, we have two fully connected layers. After these
convolution layers, we have a fully connected layer with **eighty-four neurons**. At last, we
have an output layer with **ten neurons** since the data have ten classes.

### Contributions
- **First CNN:** Developed by Yann LeCun in 1998.
- **Handwriting Recognition:** Primarily designed for character recognition.

## AlexNet
- Alexnet won the Imagenet large-scale visual recognition challenge in 2012. The model was proposed in 2012 in the research paper named Imagenet Classification with Deep Convolution Neural Network by Alex Krizhevsky and his colleagues.
- Depth of the network was increased in comparison to Lenet-5.
- The Alexnet has eight layers with learnable parameters. The model consists of five layers with a combination of max pooling followed by 3 fully connected layers and they use Relu activation in each of these layers except the output layer.
- Relu as an activation function accelerated the speed of the training process by almost six times.
- They also used the dropout layers, that prevented their model from overfitting. Further, the model is trained on the Imagenet dataset. The Imagenet dataset has almost 14 million images across a thousand classes.
### Architecture
![[Pasted image 20231203134002.png]]
![[Pasted image 20231203134613.png]]
In the architecture, the number of filters is increasing as we are going deeper. Hence it is
extracting more features as we move deeper into the architecture.
Also, the filter size is reducing, which means the initial filter was larger and as we go ahead
the filter size is decreasing, resulting in a decrease in the feature map shape.


## Lenet-5s vs Alexnet

| Feature                   | LeNet-5                                     | AlexNet                                            |
|---------------------------|---------------------------------------------|----------------------------------------------------|
| **Year Introduced**       | 1998                                        | 2012                                               |
| **Architecture**          | Shallow (7 layers including 3 convolutional) | Deep (8 layers including 5 convolutional)           |
| **Input Size**            | Small images (e.g., 32x32 pixels)           | Larger images (e.g., 227x227 pixels)               |
| **Convolutional Layers**  | Conv1: 6 filters (5x5), Conv2: 16 filters (5x5), Conv3: 120 filters (5x5) | Conv1: 96 filters (11x11, stride 4), Conv2: 256 filters (5x5), Conv3: 384 filters (3x3), Conv4: 384 filters (3x3), Conv5: 256 filters (3x3) |
| **Pooling**               | Average pooling                             | Max pooling                                        |
| **Fully Connected Layers**| Two fully connected layers at the end        | Three fully connected layers at the end            |
| **Activation Function**   | Sigmoid in the output layer                 | ReLU in convolutional layers, softmax in output layer|
| **Regularization**        | No dropout                                  | Dropout in fully connected layers                 |
| **ImageNet Challenge**    | Not applicable                              | Winner in 2012 ImageNet Challenge                  |

### Contributions
- **ImageNet Challenge:** Winner of the 2012 ImageNet Large Scale Visual Recognition Challenge.
- **Deep Learning Resurgence:** Popularized the use of deep neural networks.

## VGG Net

### Architecture
- **Convolutional Layers:**
  - Consists of 16 or 19 weight layers.
  - 3x3 convolutional filters.

- **Pooling:**
  - Max pooling after every convolutional block.

- **Fully Connected Layers:**
  - Three fully connected layers.

### Contributions
- **Simplicity:**
  - Emphasizes simplicity and depth.

- **Transfer Learning:**
  - Pre-trained models widely used for transfer learning.

## ResNet (Residual Network)
- After the first CNN-based architecture (AlexNet) that win the ImageNet 2012 competition, Every subsequent winning architecture uses more layers in a deep neural network to reduce the error rate.
- This works for less number of layers, but when we increase the number of layers, there is a common problem in deep learning associated with that called the Vanishing/Exploding gradient.
- This causes the gradient to become 0 or too large. Thus when we increases number of layers, the training and test error rate also increases.
- In order to solve the problem of the vanishing/exploding gradient, this architecture introduced the concept called Residual Blocks.
- In this network, we use a technique called skip connections.
- The skip connection connects activations of a layer to further layers by skipping some layers in between. This forms a residual block. Resnets are made by stacking these residual blocks together.

### Architecture
![[Pasted image 20231203135430.png]]
![[Pasted image 20231203135305.png]]
This network uses a 34-layer plain network architecture inspired by VGG-19 in which then the shortcut connection is added. These shortcut connections then convert the architecture into a residual network.

### Contributions
- **Overcoming Vanishing Gradient:** Addresses the vanishing gradient problem with skip connections.
- **Depth:** Extremely deep networks (50, 101, 152 layers).

## Inception Network (GoogLeNet) - V1
- Very deep networks are susceptible to overfitting. It is also hard to pass gradient updates through the entire network.
- Deep Convolutional Networks are computationally expensive. However, computational costs can be reduced drastically by introducing a **1 x 1 convolution**. Here, the number of input channels is limited by adding an extra 1×1 convolution before the 3×3 and 5×5 convolutions.
- Though adding an extra operation may seem counter-intuitive but 1×1 convolutions are far cheaper than 5×5 convolutions.
- Do note that the 1×1 convolution is introduced after the max-pooling layer, rather than before.
- At last, all the channels in the network are concatenated together i.e. (28 x 28 x (64 + 128 + 32 + 32)) = 28 x 28 x 256.
- 1 X 1 convolution: A 1×1 convolution simply maps an input pixel with all its respective channels to an output pixel. 1×1 convolution is used as a dimensionality reduction module to reduce computation to an extent.
- Sparsely connected network architectures.
### Architecture
![[Pasted image 20231203140158.png]]
![[Pasted image 20231203140326.png]]
- This architecture has 22 layers in total. 
- This is popularly known as GoogLeNet (Inception v1). GoogLeNet has 9 such inception modules fitted linearly. 
- It is 22 layers deep (27, including the pooling layers). At the end of the architecture, fully connected layers were replaced by a global average pooling which calculates the average of every feature map.
- This indeed dramatically declines the total number of parameters. Thus, Inception Net is a victory over the previous versions of CNN models. It achieves an accuracy of top-5 on ImageNet, it reduces the computational cost to a great extent without compromising the speed and accuracy.
### Contributions
- **Computational Efficiency:**
  - Achieves good performance with reduced parameters.

- **GoogLeNet:**
  - Winner of the 2014 ImageNet Challenge.



