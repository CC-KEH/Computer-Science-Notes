# Linear Regression

Linear regression is a fundamental statistical and machine learning technique used for modeling the relationship between a dependent variable (target) and one or more independent variables (predictors) by fitting a linear equation to the observed data. It is widely employed for predictive modeling, understanding relationships between variables, and making data-driven decisions.

## Key Components of Linear Regression

### 1. Linear Equation
The linear regression model assumes that the relationship between the dependent variable (Y) and independent variable(s) (X) can be expressed using a linear equation of the form:

**Simple Linear Regression:**
Y = β0 + β1 * X + ε

**Multiple Linear Regression:**
Y = β0 + β1 * X1 + β2 * X2 + ... + βn * Xn + ε

- Y: Dependent variable (the variable we want to predict).
- X1, X2, ..., Xn: Independent variables (predictors).
- β0: Intercept (the value of Y when all Xs are zero).
- β1, β2, ..., βn: Coefficients (slopes) for the respective independent variables.
- ε: Error term (represents unexplained variation in Y).

### 2. Assumptions of Linear Regression

Linear regression relies on several key assumptions, which should be met for the model to be valid:

**a. Linearity:** The relationship between independent and dependent variables is linear.

**b. Independence:** Residuals (errors) should be independent of each other.

**c. Homoscedasticity:** Residuals should have constant variance (homogeneity of variance).

**d. Normality of Residuals:** Residuals should be normally distributed.

**e. No Multicollinearity:** Independent variables should not be highly correlated with each other.

### 3. Objective Function

The objective of linear regression is to find the coefficients (β0, β1, β2, ...) that minimize the sum of squared residuals (the vertical distances between the predicted and actual values). This is known as the Ordinary Least Squares (OLS) method.

**Objective Function (Cost Function):**
J(β0, β1, β2, ...) = Σ(yi - ŷi)^2

- yi: Actual value of the dependent variable.
- ŷi: Predicted value of the dependent variable.

### 4. Optimization Algorithm

Linear regression typically uses optimization algorithms to find the values of coefficients that minimize the cost function. The most common optimization algorithm is Gradient Descent. The goal is to update the coefficients iteratively until convergence.

**Gradient Descent Update Rule (for each coefficient βj):**
βj_new = βj_old - α * ∂J(β0, β1, β2, ...)/∂βj

- α (alpha): Learning rate (controls the step size during each iteration).
- ∂J(β0, β1, β2, ...)/∂βj: Partial derivative of the cost function with respect to the j-th coefficient.

### 5. Model Evaluation

To assess the performance of a linear regression model, various metrics can be used, including:

- **R-squared (R²):** Measures the proportion of variance in the dependent variable explained by the model. R² ranges from 0 to 1, with higher values indicating a better fit.

- **Mean Squared Error (MSE):** Measures the average squared difference between predicted and actual values.

- **Root Mean Squared Error (RMSE):** The square root of the MSE, provides an interpretable measure of error in the same units as the dependent variable.

