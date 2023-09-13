# Linear Regression

**Simple Linear Regression:**
In simple linear regression, we are dealing with one independent variable (predictor) and one dependent variable (the target we want to predict). The linear equation is expressed as:

**Y = β0 + β1 * X + ε**

- **Y:** This represents the dependent variable, which is what we are trying to predict, such as housing prices or exam scores.
  
- **X:** This is the independent variable (predictor), and it represents the input feature, like the size of a house or the number of hours studied.

- **β0:** The intercept, often referred to as the bias term, represents the predicted value of Y when X is zero. It's the point where the regression line intersects the Y-axis.

- **β1:** The coefficient for X, also known as the slope, indicates how much Y changes for a unit change in X. It quantifies the strength and direction of the relationship between X and Y.

- **ε (epsilon):** The error term represents the variability in Y that is not explained by the linear relationship with X. It includes factors we can't account for in the model, such as measurement errors or unobserved variables.

**Multiple Linear Regression:**
Multiple linear regression extends the concept to multiple independent variables:

**Y = β0 + β1 * X1 + β2 * X2 + ... + βn * Xn + ε**

- In this case, we have multiple independent variables, X1, X2, ..., Xn, each with its respective coefficient (β1, β2, ..., βn). The model aims to capture the combined effect of all these variables on the dependent variable Y.

### 2. Assumptions of Linear Regression

**a. Linearity:** The linearity assumption implies that the relationship between the independent variables (X1, X2, ..., Xn) and the log-odds of the dependent variable Y is linear. This means that changes in X are associated with proportional changes in the expected value of Y.

**b. Independence:** Independence of observations means that each data point should be independent of the others. In other words, the value of Y for one data point should not be influenced by the value of Y for another data point.

**c. Homoscedasticity:** Homoscedasticity means that the variance of the residuals (the differences between observed and predicted values) should be constant across all levels of the independent variables. This assumption ensures that the model's predictions have consistent levels of accuracy throughout the range of X values.

**d. Normality of Residuals:** The normality assumption states that the residuals should follow a normal distribution, which implies that the errors have a symmetric, bell-shaped curve. This assumption is crucial for valid hypothesis testing and constructing confidence intervals.

**e. No Multicollinearity:** Multicollinearity occurs when two or more independent variables in the model are highly correlated with each other. This can lead to unstable coefficient estimates and makes it difficult to isolate the individual effects of each variable on the dependent variable.

These assumptions are essential for the accuracy and reliability of linear regression models, and violations of these assumptions can lead to inaccurate predictions and misleading results.

### 3. Objective Function

The objective of linear regression is to find the coefficients (β0, β1, β2, ...) that minimize the sum of squared residuals. The sum of squared residuals (also known as the sum of squared errors or the cost function) is defined as:

**J(β0, β1, β2, ...) = Σ(yi - ŷi)^2**

- **J(β0, β1, β2, ...):** This is the cost function, and it quantifies how well the model fits the observed data.

- **yi:** The actual value of the dependent variable (the observed value).

- **ŷi:** The predicted value of the dependent variable based on the model.

The goal of linear regression is to find the values of coefficients (β0, β1, β2, ...) that minimize this cost function. Minimizing the sum of squared residuals results in the best-fitting line or hyperplane through the data points.

### 4. Optimization Algorithm

Linear regression typically uses optimization algorithms to find the values of coefficients that minimize the cost function. The most common optimization algorithm is Gradient Descent, which iteratively updates the coefficients until convergence. The update rule for each coefficient βj is as follows:

**βj_new = βj_old - α * ∂J(β0, β1, β2, ...)/∂βj**

- **βj_new:** The new value of the j-th coefficient.
- **βj_old:** The old value of the j-th coefficient.
- **α (alpha):** The learning rate, which controls the step size during each iteration.
- **∂J(β0, β1, β2, ...)/∂βj:** The partial derivative of the cost function with respect to the j-th coefficient. It indicates the direction and magnitude of the change needed to minimize the cost.

Gradient Descent continues to update the coefficients until the cost function reaches a minimum, resulting in the best-fitting model.

### 5. Model Evaluation

To assess the performance of a linear regression model, various metrics are used:

- **R-squared (R²):** R

-squared measures the proportion of variance in the dependent variable explained by the model. It ranges from 0 to 1, where higher values indicate a better fit. An R-squared of 1 means the model explains all the variability in the data.

- **Mean Squared Error (MSE):** MSE quantifies the average squared difference between predicted and actual values. It provides a measure of the model's accuracy, with lower values indicating better performance.

- **Root Mean Squared Error (RMSE):** RMSE is the square root of MSE and provides a more interpretable measure of error in the same units as the dependent variable.

