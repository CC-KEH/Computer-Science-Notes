# Gradient Descent

- Gradient descent is an iterative optimization algorithm used to find the minimum of a function.
- It works by starting at a point and then moving in the direction of the steepest descent until it reaches a minimum.
- The steepest descent is the direction in which the function is decreasing the fastest.
- The gradient of a function is a vector that points in the direction of the steepest descent.
- The gradient descent algorithm can be used to find the minimum of any function, but it is most commonly used in machine learning to train models.


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
    - **Mini-batch gradient descent:** This is a type of gradient descent takes a subset of the entire dataset to calculate the cost function.
    - **Batch gradient descent:** Also called as vanilla gradient descent. Let’s say there are a total of ‘m’ observations in a data set and we use all these observations to calculate the cost function J, then this is known as Batch Gradient Descent. This is a type of gradient descent that updates the parameters after all of the training set i.e. epoch, that means parameters will be updated only once per [[Some terms to remember|epoch]].
- The choice of gradient descent algorithm depends on the specific problem being solved.

|Algorithm   | Updates parameters after  | Stability  | Speed  |
|---|---|---|---|
|Stochastic gradient descent (SGD)|Each training example|Low|Fast|
|Mini-batch gradient descent (MBGD)|A small batch of training examples|Medium|Medium|
|Batch gradient descent (BGD)|All of the training examples|High|Slow|

![[Pasted image 20230912204526.png]]




# Question
![[Pasted image 20230912204814.png]]