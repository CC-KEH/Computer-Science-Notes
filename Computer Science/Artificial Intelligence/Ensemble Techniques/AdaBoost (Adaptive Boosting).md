## Introduction

AdaBoost, short for Adaptive Boosting, is an ensemble learning technique designed to improve the performance of weak learners (models that perform slightly better than random chance). It operates by sequentially training a series of weak learners and assigning different weights to the training instances based on their performance. The final prediction is a weighted combination of the individual weak learners.

![[Pasted image 20231228184630.png]]

## Key Components

### 1. **Weak Learners:**
   - AdaBoost typically uses decision trees with a single level (stumps) as weak learners. These simple models are often referred to as "weak" because their predictive power is only slightly better than random chance.
### 2. **Weights:**
   - Each training instance is assigned an initial weight. Initially, all weights are set equally.
### 3. **Sequential Training:**
   - AdaBoost trains weak learners sequentially. After each iteration, it assigns higher weights to instances that were misclassified by the previous weak learners, making them more influential in subsequent rounds.
### 4. **Weighted Voting:**
   - The final prediction is determined by a weighted combination of the weak learners. Each weak learner's contribution to the final prediction is proportional to its accuracy, and more accurate models are given higher weights.

## AdaBoost Algorithm

1. **Initialize Weights:**
   - Assign equal weights to all training instances.

1. **Iterative Training:**
   - For each iteration (round):
      - Train a weak learner on the current weighted dataset.
      - Calculate the error of the weak learner, emphasizing misclassified instances.

2. **Calculate Weak Learner Weight:**
   - Calculate the weight of the weak learner based on its error rate. More accurate models receive higher weights.

3. **Update Weights:**
   - Update the weights of training instances, increasing the weights of misclassified instances.

4. **Repeat:**
   - Repeat steps 2-4 for a predefined number of iterations or until a stopping criterion is met.

5. **Final Prediction:**
   - Combine the predictions of all weak learners, giving higher weight to more accurate models.

## Advantages

1. **Adaptability:**
   - AdaBoost adapts to misclassified instances over iterations, focusing on improving the model's performance where it struggles.

2. **High Accuracy:**
   - By combining multiple weak learners, AdaBoost often achieves higher accuracy than individual models.

3. **No Hyperparameter Tuning:**
   - AdaBoost has minimal hyperparameters, reducing the need for extensive tuning.

## Challenges and Considerations

1. **Sensitive to Noisy Data:**
   - AdaBoost can be sensitive to noisy data and outliers, as it may assign too much emphasis to misclassified instances.

2. **Computational Complexity:**
   - The sequential nature of AdaBoost may limit its parallelization, making it computationally intensive.