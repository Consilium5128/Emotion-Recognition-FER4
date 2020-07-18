# Emotion-Recognition-FER4
Master Repository for all model code, Pre-processing+feature extraction+classification+validation

The Emotion Recognition using Facial Expressions project was offered by Brain and Cognitive Society, Science and Technology Council, IIT Kanpur in the summer of 2020. The project, as is self-explanatory from it's name, aims to to detect involuntary emotional response occurring simultaneously with conflicting voluntary emotional response and identifying true emotions by building classifiers that categorise facial expressions into 6 universal emotion categories (+1 neutral)

1. Anger
2. Happiness
3. Disgust
4. Fear
5. Sadness
6. Surprise
7. Neutral

## Paper
The paper which our team followed can be found [here](Li2020_Article_FacialExpressionRecognitionWit.pdf).
We didn't implement the paper exactly as it is but followed the direction specified in the paper. There are certain variations which we did to make it our own.

## Dataset
The Dataset used is the The Japanese Female Facial Expression, or JAFFE dataset. It can be found in the dataset folder [above](https://github.com/Consilium5128/Emotion-Recognition-FER4/tree/master/Dataset%20%2B%20Files)

## Verticals
1. [Pre-Processing](https://github.com/Consilium5128/Emotion-Recognition-FER4/tree/master/Pre-Processing)
2. [Feature Extraction](https://github.com/Consilium5128/Emotion-Recognition-FER4/tree/master/Feature%20Extraction)
3. [Classification](https://github.com/Consilium5128/Emotion-Recognition-FER4/tree/master/Classification)
4. [Validation](https://github.com/Consilium5128/Emotion-Recognition-FER4/tree/master/Validation)

## Code
The final code can be seen [here](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/FER4.ipynb)

## Variations from Paper
|        Paper       |      Our Model      |
| :----------------: | :----------------:  |
| Momentum optimizer |   Adam optimizer    |
| learning rate=0.001|learning rate=0.0001 |
| momentum = 0.001   |          -          |
| Dropout(0.5)       | Dropout(0.25)       |
|        -           | Local Binary Pattern|
| Epochs = 120       | Epochs = 10         |
| Batch size = 16    | Batch size=Default  |

There are a few smaller variations too in the Pre-processing code (Cropping and Alignement methods) and in validation, which opted out of using a hidden fully connected layer to improve accuracy.

## Training and Testing Data
We used Kfold Cross Validation on JAFFE dataset (with augmentation) to train the model and simultaneously test it too. No external dataset was used for testing (No cross-database testing)

## Results
The final accuracy obtained by the model was **100%** (both training and validation accuracy) with a loss of **(5.711762e-05)** on a total of **876 images** of the **JAFFE dataset** with a **10 split Kfold Cross Validation**

The accuracy obtained using the parameters of the Paper was 76.12%

The accuracy obtained without Kfold cross validation and LBP was 65.01%, while that with just Kfold was 83.91% peak accuracy (validation data)

The best accuracy obtained by the paper with the JAFFE dataset was 97.65% with an average of 97.18%

Our final model yielded the highest accuracy of 100% which was almost consistent after the 3rd epoch. There were differences noticed in the training times too as our model required 51 minutes at max to train while on the same computer, it required approximately 9 hours to train using the paper's parameters.

## Visualization
**Initial Image**  
![Initial Image](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Initial%20Image.png)

**Image after cropping**  
![Cropping](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Image%20after%20cropping.png)

**Image after Histogram Equalization**  
![Histogram Equalization](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Image%20after%20histogram%20equalization.png)

**Image after Flipping**  
![Flip](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Flipped%20image.png)

**Image after noise addition**  
![Noise addition](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Image%20after%20noise%20addition.png)

**LBP Histogram**  
![Histogram](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/LBP%20Histogram.png)

**CNN model structure**
![CNN model](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/CNN%20model%20structure.png)

**Model.evaluate()**  
![Evaluate](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Model.evaluate().png)

**Accuracy Plot**  
![Accuracy](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Accuracy%20plot.png)

**Loss Plot**  
![Loss](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Loss%20plot.png)

**Confusion Matrix**  
![Confusion Matrix](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Confusion%20Matrix.png)

**Normalized Confusion Matrix**  
![Normal Confusion Matrix](https://github.com/Consilium5128/Emotion-Recognition-FER4/blob/master/Images_Visualization/Normalized%20Confusion%20Matrix.png)

## Impact
In this project , we present an efficient FER approach which simplifies the CNN and propose new face cropping and image rotation methods.
 We envision that these proposed data processing methods will lead to high recognition accuracies and can be implemented on an ordinary computer without GPU acceleration. We hope our effort will act as catalyst for deeper research in this field and someday these techniques will be used in consumer neuroscience & neuromarketing and medical applications & plastic surgery.

## Team

Mentor - Avisha Gaur

Team - 
Falguni Yadav,
Prachi Singh,
Pranav Kumar,
Saksham Pruthi,
Samriddhi Gupta,
Tanisha Agrawal,
Videeta Sharma,
Yatharth Gupta
