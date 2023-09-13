
# Linear Regression VS. Logistic Regression

| Feature                              | Linear Regression                               | Logistic Regression                           |
|--------------------------------------|-------------------------------------------------|----------------------------------------------|
| **Type of Problem**                  | Regression                                       | Classification                                |
| **Dependent Variable**               | Continuous (numeric)                            | Binary (0 or 1) or Multiclass                |
| **Output**                           | Predicts a continuous value                     | Predicts probabilities or classes             |
| **Equation**                         | \(y = \beta_0 + \beta_1x_1 + \beta_2x_2 + \ldots + \beta_nx_n\) | \(p(y=1) = \frac{1}{1 + e^{-(\beta_0 + \beta_1x_1 + \beta_2x_2 + \ldots + \beta_nx_n)}}\) |
| **Range of Predictions**             | \(-\infty\) to \(+\infty\)                     | \(0 \leq p(y=1) \leq 1\)                      |
| **Output Interpretation**            | Represents the expected value of the dependent variable given the input features. | Represents the probability of belonging to a specific class given the input features. |
| **Assumption of Linearity**          | Assumes a linear relationship between the independent and dependent variables. | Assumes a linear relationship between the log-odds of the dependent variable and the independent variables. |
| **Error Calculation**                | Typically uses Mean Squared Error (MSE) or other regression-related metrics. | Uses log-likelihood, cross-entropy, or other classification-related metrics like accuracy, precision, recall, F1-score, AUC-ROC, etc. |
| **Applications**                     | Used for predicting continuous values, e.g., predicting house prices, stock prices, etc. | Used for classification tasks like spam detection, disease diagnosis, customer churn prediction, etc. |
| **Example Libraries**                | Scikit-Learn, TensorFlow, PyTorch, etc.          | Scikit-Learn, TensorFlow, PyTorch, etc.      |
| **Regularization**                    | Ridge, Lasso, Elastic Net, etc., can be used for regularization. | Regularization techniques like L2 regularization can be applied. |
| **Sensitivity to Outliers**           | Sensitive; outliers can significantly impact the regression line. | Less sensitive due to the logistic function's saturation at extreme values. |
| **Output Type**                      | Continuous (numeric)                            | Probabilities or class labels                |
| **Model Evaluation**                 | Metrics like RMSE, MAE, R-squared, etc.        | Metrics like accuracy, precision, recall, F1-score, AUC-ROC, etc. |
| **Estimation Method**                | Based on Least Squares: Minimizes the sum of squared differences between observed and predicted values. | Based on Maximum Likelihood Estimation: Maximizes the likelihood of the observed outcomes given the model parameters. |
| **Distribution Assumption**           | Assumes normal distribution for the dependent variable. | Assumes a binomial (binary) or multinomial (multiclass) distribution for the dependent variable. |
| **Coefficient Interpretation**        | Coefficients (\(\beta\)) represent the change in the dependent variable for a one-unit change in the corresponding independent variable. | Coefficients (\(\beta\)) represent the change in the log-odds of the dependent variable for a one-unit change in the corresponding independent variable. |
| **Heteroscedasticity Handling**       | Sensitive to heteroscedasticity; assumes constant variance (homoscedasticity) of errors. | Less sensitive to heteroscedasticity; doesn't assume constant variance. |
| **Decision Boundary**                | Doesn't have a specific decision boundary; predicts values along a continuous spectrum. | Uses a sigmoid function to create an S-shaped decision boundary that separates classes. |
| **Transformation**                   | No transformation is applied to the dependent variable or the output. | Applies the logistic (sigmoid) function to transform the output into probabilities. |
| **Outliers Handling**                | Outliers can significantly influence the regression line. | Logistic regression is less sensitive to outliers due to the logistic function's saturation at extreme values. |
| **Link Function**                    | Linear regression uses the identity function as the link function. | Logistic regression uses the logistic (sigmoid) function as the link function. |
| **Multi-Collinearity Handling**       | Sensitive to multicollinearity (high correlation between independent variables). | Can handle multicollinearity relatively better. |
| **Performance Visualization**         | Scatter plots and regression lines are used to visualize results. | ROC curves, confusion matrices, and decision boundaries are used for visualization in logistic regression. |
| **Distribution of Dependent Variable**| Assumes normal distribution.                    | Assumes a binomial distribution for binary logistic regression; multinomial distribution for multinomial logistic regression. |
| **Estimation Basis**                 | Least Squares: Minimizes squared differences between observed and predicted values. | Maximum Likelihood Estimation: Maximizes the likelihood of observed outcomes given model parameters. |

