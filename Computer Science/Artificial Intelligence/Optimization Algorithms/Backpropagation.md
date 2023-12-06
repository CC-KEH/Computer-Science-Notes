# Definition
- It works on supervised learning
- Backpropagation is a widely used algorithm for training feedforward neural networks. It computes the gradient of the **loss function with respect to weights**.
- The backpropagation algorithm works by computing the gradient of the loss function with respect to each weight via the chain rule, computing the gradient layer by layer, and iterating backward from the last layer.
- Can learn to solve **linearly inseparable** problems.

# Working
![[Pasted image 20231206172953.png]]
![[Pasted image 20231206173006.png]]
![[Pasted image 20231206173041.png]]
![[Pasted image 20231206173058.png]]

# Limitations
1. **Local Minimum Problem:**
   - Backpropagation may get stuck in local minima during optimization, especially in high-dimensional spaces. However, modern deep learning frameworks often use techniques like weight initialization and stochastic optimization to mitigate this problem.

2. **Vanishing and Exploding Gradients:**
   - In deep neural networks, the gradients of the loss function with respect to the weights can become very small (vanishing gradients) or very large (exploding gradients) during training. This can make it challenging for the network to learn effectively, especially in deep architectures.

3. **Dependency on Initial Weights:**
   - The performance of the neural network can be sensitive to the initial weights. Poor initialization may lead to slow convergence or convergence to suboptimal solutions.

4. **Hyperparameter Sensitivity:**
   - Backpropagation requires tuning various hyperparameters such as learning rate, batch size, and regularization strength. The algorithm's performance can be sensitive to the choice of these hyperparameters, and finding optimal values may require experimentation.

5. **Overfitting:**
   - Neural networks trained using backpropagation are prone to overfitting, especially when the model is too complex relative to the size of the dataset. Regularization techniques, such as dropout and L2 regularization, are often employed to address this issue.

6. **Requires Labeled Data:**
   - Backpropagation requires labeled training data for supervised learning. It cannot be directly applied to unsupervised or reinforcement learning scenarios without modifications or additional techniques.

7. **Limited Interpretability:**
   - Neural networks trained with backpropagation are often treated as "black-box" models, making it challenging to interpret and understand how they arrive at specific predictions. Interpretability is crucial, especially in applications where decisions impact human lives (e.g., healthcare).

8. **Computational Intensity:**
   - Training deep neural networks using backpropagation can be computationally intensive, requiring significant resources. This limitation has led to the development of more efficient training algorithms and hardware accelerators.

9. **Data Quality Dependency:**
   - The performance of backpropagation is highly dependent on the quality and representativeness of the training data. Biased or unrepresentative datasets can lead to biased models.

10. **Catastrophic Forgetting:**
    - In certain scenarios, especially with sequential learning or continual learning, neural networks trained with backpropagation can forget previously learned information when exposed to new data. This is known as catastrophic forgetting.