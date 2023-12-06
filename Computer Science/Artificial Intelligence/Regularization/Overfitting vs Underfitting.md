# Overfitting
- Overfitting is a phenomenon in which The learned model works well for training data but terrible for testing data (unknown data). In other words, the model has little training error but has huge perdition error.
- That is when our model learns the noise in the training data as well.
- This is the case when our model memorizes the training data instead of learning the patterns in it.
- Such models usually perform very well on training data but have high error rates on test data. High Variance causes overfitting in our model.
- Variance defines the algorithm’s sensitivity to specific sets of data.
- A model with a high variance pays a lot of attention to training data and does not generalize therefore the validation error or prediction error are far apart from each other.
![[Pasted image 20231206173922.png]]

# Underfitting
- Underfitting on the other hand is the case when our model is not able to learn even the basic patterns available in the dataset.
- In the case of the underfitting model is unable to perform well even on the training data hence we cannot expect it to perform well on the test data.
- This is the case when we are supposed to increase the complexity of the model or add more features to the feature set.
- High Bias causes underfitting in our model. 
- Bias occurs when an algorithm has limited flexibility to learn from data.
- Such models pay very little attention to the training data and oversimplify the model therefore the validation error or prediction error and training error follow similar trends.
![[Pasted image 20231206174042.png]]

![[Pasted image 20231206174029.png]]



# Now What?
- An optimal model is one in which the model is sensitive to the pattern in our model, but at the same time can generalize to new data. This happens when Bias and Variance are both optimal.
- To avoid these problems we use [[Computer Science/Artificial Intelligence/Regularization/Regularization|Regularization]]Techniques
