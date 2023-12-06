# Introduction
- L1 and L2 are the most common types of regularization. These update the general cost function by adding another term known as the regularization term.

- Cost function = Loss (say, binary cross entropy) + Regularization term

- Due to the addition of this regularization term, the values of weight matrices decrease because it assumes that a neural network with smaller weight matrices leads to simpler models. Therefore, it will also reduce overfitting to quite an extent.

- In machine learning that regularization penalizes the **coefficients**. In deep learning, it actually penalizes the **weight matrices** of the nodes.


# Lasso Regression (L1)
- A regression model which uses the L1 Regularization technique is called LASSO(Least Absolute Shrinkage and Selection Operator) regression. Lasso Regression adds the “absolute value of magnitude” of the coefficient as a penalty term to the loss function(L).

- Lasso regression also helps us achieve **feature selection** by penalizing the weights (w) to approximately equal to zero if that feature does not serve any purpose in the model.


# Ridge Regression (L2)
- Also known as Ridge Regularization, it modifies the over-fitted or under fitted models by adding the penalty equivalent to the sum of the squares of the magnitude of coefficient.



# Difference
L1 and L2 regularization are two common techniques used to prevent overfitting in machine learning models by adding a penalty term to the loss function. They are named after the norms they use to calculate the regularization term.

### L1 Regularization (Lasso):
1. **Regularization Term:**
   - **Formula:** \( \lambda \sum_{i=1}^{n} \lvert w_i \rvert \), where \( \lambda \) is the regularization strength and \( w_i \) are the model parameters.

2. **Effect on Weights:**
   - L1 regularization encourages sparsity in the weights. It tends to force some weights to be exactly zero, effectively performing feature selection.

3. **Use Case:**
   - L1 regularization is often preferred when there is a belief that many features are irrelevant or when feature selection is desirable.

4. **Robustness to Outliers:**
   - L1 regularization can be sensitive to outliers in the data.

5. **Optimization Algorithm:**
   - L1 regularization introduces non-differentiability due to the absolute value function, so it requires subgradient methods for optimization.

### L2 Regularization (Ridge):
1. **Regularization Term:**
   - **Formula:** \( \frac{\lambda}{2} \sum_{i=1}^{n} w_i^2 \), where \( \lambda \) is the regularization strength and \( w_i \) are the model parameters.

2. **Effect on Weights:**
   - L2 regularization penalizes large weights but does not force them to be exactly zero. It tends to evenly reduce the impact of all features.

3. **Use Case:**
   - L2 regularization is commonly used when all features are expected to contribute to the model, and there is no prior belief that some features should be exactly zero.

4. **Robustness to Outliers:**
   - L2 regularization is less sensitive to outliers compared to L1 regularization.

5. **Optimization Algorithm:**
   - L2 regularization introduces differentiability, simplifying optimization. It allows the use of standard gradient descent optimization methods.

# Combined L1 and L2 Regularization (Elastic Net):
1. **Regularization Term:**
   - **Formula:** \( \lambda_1 \sum_{i=1}^{n} \lvert w_i \rvert + \frac{\lambda_2}{2} \sum_{i=1}^{n} w_i^2 \), where \( \lambda_1 \) and \( \lambda_2 \) are the regularization strengths.

2. **Use Case:**
   - Elastic Net combines both L1 and L2 regularization, providing a balance between feature selection (sparsity) and weight shrinkage.

3. **Robustness to Outliers:**
   - Elastic Net inherits the robustness properties of L2 regularization.
