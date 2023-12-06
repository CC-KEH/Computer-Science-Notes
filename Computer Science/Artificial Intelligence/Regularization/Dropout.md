- This is the one of the most interesting types of regularization techniques. It also produces very good results and is consequently the most frequently used regularization technique in the field of deep learning.

- At every iteration, it randomly selects some nodes and removes them along with all of their incoming and outgoing connections as shown below.

- So each iteration has a different set of nodes and this results in a different set of outputs. It can also be thought of as an ensemble technique in machine learning.

- Ensemble models usually perform better than a single model as they capture more randomness. Similarly, dropout also performs better than a normal neural network model.

- This probability of choosing how many nodes should be dropped is the hyperparameter of the dropout function. Dropout can be applied to both the hidden layers as well as the input layers.

- Due to these reasons, dropout is usually preferred when we have a large neural network structure in order to introduce more randomness.


![[Pasted image 20231206175728.png]]

