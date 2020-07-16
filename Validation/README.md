After Classification is done , we run K-fold cross validation (with k=10) to measure accuracy of the neural network.
Since the dataset used is not skewed , accuracy can be used as an appropriate evaluation metric for the neural network.

In 10-fold cross validation, the entire dataset is divided into 10 parts.
One part is used as the testing data and the rest 9 part constitute the training data for the neural network.
More specifically, in 10-fold cross validation the 10 parts iterate through a cycle in which each one of these parts become the testing data and the remaining 9 parts 
constitue the training data.
As a result the computation time is reduced, the bias and variance is reduced (preventing underfitting and overfitting) because every datapoint gets to be tested 
once.

We test the structure of the neural network by adding a hidden fully connected layer and comparing the accuracies for different number of neurons in this layer [0,256,512,1024] . We find maximum average accuracy for 0 , i.e the neural network structure is better without the hidden fully connected layer.

LIBRARIES USED-
numpy and
Sklearn

EXPECTED RESULT-
A trained neural network free of underfitting or overfitting 

REFERENCES-
1. www.scikit-learn.org
2. www.machinelearningmastery.com
