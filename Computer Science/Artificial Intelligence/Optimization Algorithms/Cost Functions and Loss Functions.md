## Definition:

Cost functions and loss functions are mathematical tools used in supervised learning to quantify the discrepancy between predicted values and actual values.

## Purpose:

The primary goal is to measure and minimize the error, guiding the training process towards better model parameters and more accurate predictions.

## Cost Function in Training:

During model training, the objective is to minimize the cost function, leading to improved model performance.

## Loss Function:

The terms "cost function" and "loss function" are often used interchangeably, where "loss" may refer to the error for a single training example, and "cost" is the average loss over the entire training dataset.

## Common Types of Loss Functions:

### 1. Mean Squared Error (MSE):

- **Purpose:** Widely used for regression problems, penalizing large errors quadratically.

### 2. Mean Absolute Error (MAE):

- **Purpose:** Measures the average absolute difference between predicted and actual values.

### 3. Cross-Entropy Loss (Log Loss):

- **Purpose:** Commonly used for binary and multiclass classification problems.

### 4. Hinge Loss (SVM):

- **Purpose:** Used in Support Vector Machines (SVM) for classification.

### 5. Huber Loss:

- **Purpose:** Combines the best properties of mean squared error and mean absolute error. It is less sensitive to outliers than mean squared error and provides a balance between robustness and efficiency.
