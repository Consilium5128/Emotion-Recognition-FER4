An array of labels is created corresponding to the training set images where the labels are :-anger,happy,disgust,fear,sad,surprise,neutral
Pre proccessing for each emotion file is done separately.

We have used the following methods in pre processing:
1. Face detection 
   This technique is responsible for selecting the ROI of an input image that will be fed to the next steps of the FER system.
   The images are first converted into gray images followed by face detection using haarcascade fontalface detector.

2. Face alignment(rotation correction)
   We used the facial landmarks outputted by "shape_predictor_5_face_landmarks".
   To perform face alignment of a rotated face, a rotation transformation is applied to align two facial landmarks(centre of both the eyes) with the horizontal axis, until the angle formed by them is zero.

3. Data normalization(Histogram equilization)
   Because of potential different lighting conditions that extracted faces may present, the recognition accuracy will likely suffer.
   So we used algorithms of cv2(cv2.equalizeHist(img)) for histogram equilization.

4. Data augmentation
   Since a small dataset can lead to overfitting, we performed random rotation, random noise and horizontal flipping on pre-processed images to increase the dataset.
   We have used algorithms of skimage for this.

All the images after preprocessing along with augmentated images are appended in a list and we get a final list of pre processed data which will be used further.
The link for the codes of all the pre processing steps is here-

LIBRARIES USED-dlib,cv2,numpy,matplotlib,os,skimage, keras.preprocessing.image

FILES USED-"shape_predictor_5_face_landmarks.dat.bz2",'haarcascade_frontalface_default.xml'

FINAL OUTPUT- Images can be viewed in the [Image_Visualisation](https://github.com/Consilium5128/Emotion-Recognition-FER4/tree/master/Images_Visualization) folder
