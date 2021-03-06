After Pre-processing and Feature Extraction, a CNN model had been used to classify the images into one of the 6 emotions (+1 neutral) based on numeric labels assigned to each of the emotions beforehand.

Two models were predefined and the final CNN model that had been used is the one which was specified by the paper, with a variation in Dropout value to achieve optimum accuracy.

Xavier initializer had been used which ensures that the mean of the activations should be zero and the variance of the activations should stay the same across every layer, coupled with Relu activation function along with the Adam optimizer.
Learning Rate = 0.0001

Libraries used:

numpy, tensorflow (tensorflow.keras)

References:
1. https://keras.io/api/layers/initializers/
2. https://keras.io/api/optimizers/
3. https://www.tensorflow.org/api_docs/python/tf/keras/Model  
4. https://towardsdatascience.com/weight-initialization-in-neural-networks-a-journey-from-the-basics-to-kaiming-954fb9b47c79

