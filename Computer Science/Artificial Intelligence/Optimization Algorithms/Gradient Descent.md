# Gradient Descent

- Gradient descent is an iterative optimization algorithm used to find the minimum of a function.
- It works by starting at a point and then moving in the direction of the steepest descent until it reaches a minimum.
- The steepest descent is the direction in which the function is decreasing the fastest.
- The gradient of a function is a vector that points in the direction of the steepest descent.
- The gradient descent algorithm can be used to find the minimum of any function, but it is most commonly used in machine learning to train models.

![[1_laN3aseisIU3T9QTIlob4Q.gif]]


### Advantages and Disadvantages of Gradient Descent

- Gradient descent is a simple and efficient algorithm.
- It can be used to find the minimum of any function.
- It is relatively easy to implement.
- However, gradient descent can be slow to converge, especially for large and complex functions.
- It can also be sensitive to the choice of hyperparameters, such as the learning rate.


## How Gradient Descent works

**1. Initialize the parameters.** The first step is to initialize the parameters of the model. These are the weights and biases of the network. The parameters can be initialized randomly or by using a pre-trained model.

- **Random initialization:** Random initialization is a common way to initialize the parameters of a machine learning model. This means randomly assigning values to the weights and biases of the network. Random initialization helps to prevent the model from getting stuck in a local minimum.
- **Pre-trained model:** A pre-trained model is a model that has already been trained on a large dataset. The parameters of a pre-trained model can be used to initialize the parameters of a new model. This can help to speed up the training process and improve the performance of the new model.

**2. Calculate the gradient.** The next step is to calculate the gradient of the cost function with respect to the parameters. The gradient is a vector that points in the direction of the steepest descent.

- **Cost function:** The cost function is a measure of how well the model is performing. The goal of gradient descent is to find the values of the parameters that minimize the cost function.
- **Gradient:** The gradient of the cost function with respect to the parameters is a vector that points in the direction of the steepest descent. This means that the gradient points in the direction of the change that will cause the cost function to decrease the most.

**3. Update the parameters.** The gradient points in the direction of the steepest descent, so we can update the parameters by moving them in the opposite direction. The amount by which we move the parameters is determined by the learning rate.

- **Learning rate:** The learning rate is a hyperparameter that controls how much the parameters are updated in each iteration. A smaller learning rate will make the algorithm converge more slowly, but it will be more stable. A larger learning rate will make the algorithm converge more quickly, but it may be more likely to overshoot the minimum.

**4. Repeat steps 2 and 3 until convergence.** We repeat steps 2 and 3 until the cost function converges, which means that it has reached a minimum.

The gradient descent algorithm will continue to update the parameters until the cost function no longer decreases. This means that the algorithm has reached a minimum.


**Convergence Algorithm:**
```go 
xn+1​ = xn - α * ∇f(xn​)
```
- xn​ is the value of the parameters at the current iteration
- xn+1​ is the value of the parameters at the next iteration
- α is the learning rate
- ∇f(xn​) is the gradient of the cost function with respect to the parameters at the current iteration

## When should I use Gradient descent?
- Works well even when n is massive (millions)
- Better suited to big data
- What is a big n though
- 100 or even a 1000 is still (relativity) small
- If n is 10 000 then look at using gradient descent

## Effects of Learning rate on Gradient Descent
![[Pasted image 20230912203128.png]]



## Types of Gradient Descent

- There are many different types of gradient descent algorithms.
- Some of the most common types are:
    - **Stochastic gradient descent:** If you use a single observation to calculate the cost function it is known as Stochastic Gradient Descent, commonly abbreviated as SGD. We pass a single observation at a time, calculate the cost and update the parameters.
	    - Pseudocode![[Pasted image 20231206233915.png]]
    - **Mini-batch gradient descent:** This is a type of gradient descent takes a subset of the entire dataset to calculate the cost function. mixture of Stochastic and Batch Gradient Descent.
	    - Pseudocode![[Pasted image 20231206234613.png]]
    - **Batch gradient descent:** Also called as vanilla gradient descent. Let’s say there are a total of ‘m’ observations in a data set and we use all these observations to calculate the cost function J, then this is known as Batch Gradient Descent. This is a type of gradient descent that updates the parameters after all of the training set i.e. epoch, that means parameters will be updated only once per [[Some terms to remember|epoch]].
	    - Pseudocode![[Pasted image 20231206233630.png]]
- The choice of gradient descent algorithm depends on the specific problem being solved.

|Algorithm   | Updates parameters after  | Stability  | Speed  |
|---|---|---|---|
|Stochastic gradient descent (SGD)|Each training example|Low|Fast|
|Mini-batch gradient descent (MBGD)|A small batch of training examples|Medium|Medium|
|Batch gradient descent (BGD)|All of the training examples|High|Slow|

![[Pasted image 20230912204526.png]]




## Challenges of Gradient Descent and Optimization Algorithms:

1. **Convergence Speed:**
   - **Issue:** Traditional gradient descent may converge slowly, especially in cases where the cost surface has complex shapes, plateaus, or narrow valleys.
   - **Solution:** Various optimization algorithms aim to accelerate convergence.

2. **Sensitivity to Initial Conditions:**
   - **Issue:** The choice of initial parameter values can influence convergence or lead to convergence to suboptimal solutions.
   - **Solution:** Initialization strategies and advanced optimization methods can mitigate sensitivity to initial conditions.

3. **Local Minima and Saddle Points:**
   - **Issue:** Gradient descent can get stuck in local minima or slow down around saddle points, hindering convergence to the global minimum.
   - **Solution:** Optimization algorithms introduce modifications to navigate through local minima and saddle points more effectively.

4. **Learning Rate Selection:**
   - **Issue:** Choosing an appropriate learning rate is challenging. A too small learning rate can lead to slow convergence, while a too large one may cause divergence or overshooting.
   - **Solution:** Adaptive learning rate methods dynamically adjust the learning rate during training.

### Optimization Algorithms:

#### 1. **[[Stochastic Gradient Descent (SGD)]]:**
   - **Idea:** Instead of using the entire dataset for each iteration, SGD uses a random subset (mini-batch) to update parameters.
   - **Advantage:** Faster convergence, especially in large datasets.

#### 2. **[[Mini-Batch Gradient Descent]]:**
   - **Idea:** A compromise between SGD and batch gradient descent, where updates are computed using a small randomly selected subset (mini-batch) of the data.
   - **Advantage:** Balances the benefits of SGD (faster updates) and batch gradient descent (smoother convergence).

#### 3. **[[Momentum]]:**
   - **Idea:** Introduces a momentum term that accelerates the optimization by adding a fraction of the previous update to the current update. 
   - **Advantage:** Helps navigate through plateaus and accelerates convergence, reducing oscillations.

#### 4. **[[Adagrad (Adaptive Gradient Algorithm)]]:**
   - **Idea:** Adapts the learning rate individually for each parameter based on historical gradients. (Basically it just penalizes weights that went through a lot of changes, as compared to those who haven't gone that much. In short this is very good for sparse features)
   - **Advantage:** Well-suited for sparse data, adjusts learning rates automatically for each parameter.

#### 5. **[[RMSprop (Root Mean Square Propagation)]]:**
   - **Idea:** Similar to Adagrad but uses a moving average of squared gradients, preventing the learning rate from decreasing too rapidly.
   - **Advantage:** Addresses the diminishing learning rate problem in Adagrad.

#### 6. **[[Adam (Adaptive Moment Estimation)]]:**
   - **Idea:** Combines aspects of momentum and RMSprop, maintaining both a moving average of gradients and a moving average of squared gradients.
   - **Advantage:** Efficiently adapts learning rates and handles sparse gradients.

#### 7. **[[Nadam]]:**
   - **Idea:** An extension of Adam with Nesterov momentum, combining the benefits of Nesterov Accelerated Gradient (NAG) and Adam.
   - **Advantage:** Improved convergence on non-convex surfaces.

#### 8. **[[Adadelta]]:**
   - **Idea:** An extension of RMSprop that eliminates the need for an initial learning rate, using a running average of squared parameter updates.
   - **Advantage:** Adapts learning rates more effectively without the need for manual tuning.


# Question
![[Pasted image 20230912204814.png]]





![[0_YmOoWW7_5-St1t3I.gif]]