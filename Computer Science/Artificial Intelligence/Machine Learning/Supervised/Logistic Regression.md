# Logistic Regression

Logistic Regression is a popular statistical and machine learning technique used for binary classification tasks. It models the probability that a given instance belongs to a particular class by fitting a logistic (S-shaped) curve to the observed data. Despite its name, logistic regression is used for classification, not regression.

## Key Components of Logistic Regression

### 1. Logistic Function (Sigmoid)
The logistic regression model uses the logistic function (also known as the sigmoid function) to transform the linear combination of input features into a probability value between 0 and 1:

**Logistic Function (Sigmoid):**
p(Y=1|X) = 1 / (1 + e^(-z))

- p(Y=1|X): Probability that the instance belongs to class 1.
- X: Independent variables (predictors).
- z: Linear combination of coefficients and independent variables (z = β0 + β1 * X1 + β2 * X2 + ... + βn * Xn).

### 2. Assumptions of Logistic Regression

Logistic regression relies on several assumptions:

**a. Linearity:** The relationship between independent variables and the log-odds of the dependent variable is linear.

**b. Independence of Observations:** Each observation should be independent of the others.

**c. No Multicollinearity:** Independent variables should not be highly correlated.

**d. Large Sample Size:** Logistic regression works well with a reasonably large sample size.

### 3. Objective Function

The objective of logistic regression is to maximize the likelihood of the observed data given the model parameters (coefficients). This is done using a process called Maximum Likelihood Estimation (MLE).

**Objective Function (Likelihood Function):**
L(β0, β1, β2, ...) = Π(p(Yi|Xi)^yi * (1 - p(Yi|Xi))^(1-yi))

- L(β0, β1, β2, ...): Likelihood function.
- yi: Actual class label (0 or 1) for the i-th instance.
- p(Yi|Xi): Predicted probability of class 1 for the i-th instance.

The goal is to find the values of coefficients (β0, β1, β2, ...) that maximize the likelihood function.

### 4. Optimization Algorithm

Logistic regression typically uses optimization algorithms to find the values of coefficients that maximize the likelihood function. The most common optimization algorithm is Gradient Descent or variants like Stochastic Gradient Descent (SGD).

**Gradient Descent Update Rule (for each coefficient βj):**
βj_new = βj_old + α * ∂L(β0, β1, β2, ...)/∂βj

- α (alpha): Learning rate (controls the step size during each iteration).
- ∂L(β0, β1, β2, ...)/∂βj: Partial derivative of the likelihood function with respect to the j-th coefficient.

### 5. Model Evaluation

To assess the performance of a logistic regression model for binary classification, various metrics can be used, including:

- **Accuracy:** Measures the proportion of correctly classified instances.

- **Precision:** Measures the proportion of true positive predictions among all positive predictions.

- **Recall (Sensitivity):** Measures the proportion of true positive predictions among all actual positives.

- **F1-Score:** A balanced metric that combines precision and recall.

- **ROC Curve and AUC:** Receiver Operating Characteristic curve and Area Under the Curve, which evaluate the model's ability to distinguish between classes.
