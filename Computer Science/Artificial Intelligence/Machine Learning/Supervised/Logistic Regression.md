# Logistic Regression

Logistic Regression is a widely used statistical and machine learning technique for binary classification tasks, modeling the probability that a given instance belongs to a particular class. It employs a logistic (S-shaped) function to transform the linear combination of input features into a probability value between 0 and 1. Let's delve deeper into its key components and concepts:

### 1. Logistic Function (Sigmoid)

**Logistic Function (Sigmoid):**
The logistic regression model uses the sigmoid function to map the linear combination of input features to a probability value of belonging to class 1:

**p(Y=1|X) = 1 / (1 + e^(-z))**

- **p(Y=1|X):** Probability that an instance belongs to class 1.
- **X:** Independent variables (predictors).
- **z:** Linear combination of coefficients (β0, β1, β2, ...) and independent variables (X1, X2, ...).

The sigmoid function ensures that the output is bounded between 0 and 1, making it suitable for binary classification. It produces an S-shaped curve, allowing the model to capture nonlinear relationships.

### 2. Assumptions of Logistic Regression

**a. Linearity:** The relationship between independent variables and the log-odds of the dependent variable is linear. In simpler terms, the log-odds change linearly with changes in the independent variables. The linearity assumption can be extended using techniques like polynomial regression.

**b. Independence of Observations:** The assumption of independence states that each observation is independent of others in the dataset. Violations of this assumption can lead to unreliable model parameter estimates and hypothesis tests.

**c. No Multicollinearity:** Logistic regression assumes that independent variables are not highly correlated with each other. Multicollinearity can make it challenging to interpret the individual effects of predictors and can lead to unstable coefficient estimates.

**d. Large Sample Size:** Logistic regression generally works well with reasonably large sample sizes. Smaller sample sizes may lead to less reliable results, especially for rare events, and can affect the stability of coefficient estimates.

### 3. Objective Function

**Objective Function (Likelihood Function):**
In logistic regression, the objective is to maximize the likelihood of the observed data given the model parameters (coefficients) using Maximum Likelihood Estimation (MLE):

**L(β0, β1, β2, ...) = Π(p(Yi|Xi)^yi * (1 - p(Yi|Xi))^(1-yi))**

- **L(β0, β1, β2, ...):** Likelihood function.
- **yi:** Actual class label (0 or 1) for each instance.
- **p(Yi|Xi):** Predicted probability of class 1 for each instance.

The likelihood function quantifies how likely the observed data is under the model. The goal is to find coefficients (β0, β1, β2, ...) that maximize this likelihood function.

### 4. Optimization Algorithm

Logistic regression typically uses optimization algorithms (e.g., Gradient Descent) to find optimal coefficients. The update rule for each coefficient is:

**βj_new = βj_old + α * ∂L(β0, β1, β2, ...)/∂βj**

- **α (learning rate):** Controls step size during iterations. It's important to choose an appropriate learning rate to ensure convergence without overshooting or diverging.

- **∂L(β0, β1, β2, ...)/∂βj:** This represents the partial derivative of the likelihood function with respect to the j-th coefficient. It guides the direction of coefficient updates.

The optimization process continues until the algorithm converges to maximize the likelihood, effectively making the model as likely as possible to produce the observed data.

### 5. Model Evaluation

**Model Evaluation Metrics:**
To assess logistic regression performance:

- **Accuracy:** Measures the proportion of correctly classified instances. It's a straightforward metric but may not be suitable for imbalanced datasets.

- **Precision:** Precision measures the proportion of true positives among positive predictions. It's essential when false positives are costly, such as in medical diagnoses.

- **Recall (Sensitivity):** Recall measures the proportion of true positives among actual positives. It's crucial when false negatives are costly, such as in identifying diseases.

- **F1-Score:** The F1-Score is the harmonic mean of precision and recall, providing a balance between the two metrics. It's useful when there's a trade-off between precision and recall.

- **ROC Curve and AUC:** The Receiver Operating Characteristic (ROC) curve and Area Under the Curve (AUC) assess the model's ability to distinguish between classes across different threshold values. AUC quantifies the model's overall performance.
