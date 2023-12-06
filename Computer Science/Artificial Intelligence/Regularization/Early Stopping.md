- Early stopping is one of the regularization techniques which solves the problem of overfitting caused due to excessive training of our model.

- By training our model for a longer amount of time, we mean training our model for a large number of epochs. In deep learning, an epoch is defined as the number of times our model is trained on the entire dataset.

- It is crucial to choose the number of epochs so that it leads to an optimal model. Choosing a very low number for the epochs will lead to an underfit model, and choosing a very high number of epochs will lead to overfitting.

- For choosing an optimal number of epochs, we can use early stopping. We can choose an arbitrarily high number of epochs, and early stopping will stop the training as soon as we start to overfit our data.

- In early stopping, During the training of our model, we also check the prediction accuracy of our model on a validation dataset. We keep track of the prediction accuracy on the validation dataset, and as soon as the validation accuracy starts to decrease, we stop our training preventing overfitting.