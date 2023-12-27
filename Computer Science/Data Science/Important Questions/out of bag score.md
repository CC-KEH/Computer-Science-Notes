The out-of-bag (OOB) score is a metric used in ensemble learning, particularly in bagging algorithms like Random Forest. The term "out-of-bag" refers to the data that is not included in the bootstrap sample used to train an individual base model (tree in the case of Random Forest).

1. **Bootstrap Sampling:**
   - During the training of each tree in the Random Forest, a random subset of the original dataset is sampled with replacement. This means that some instances from the original dataset may be selected multiple times, **while others may not be selected at all**.

2. **Out-of-Bag Instances:**
   - _The instances that are not included in the bootstrap sample for a particular tree are referred to as out-of-bag instances_. Since these instances were not used to train the tree, they essentially serve as a test set for that specific tree.

3. **Out-of-Bag Score Calculation:**
   - Once all the trees are trained, each instance in the dataset has been left out of the training set for some trees. The out-of-bag score is calculated by aggregating the predictions of each instance across all the trees where it served as an out-of-bag instance.

4. **Performance Evaluation:**
   - The aggregated out-of-bag predictions can be compared to the true labels to evaluate the performance of the Random Forest. This provides an estimate of how well the model might generalize to unseen data.