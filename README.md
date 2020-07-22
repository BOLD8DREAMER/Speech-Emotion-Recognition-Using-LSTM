# Speech Emotion Recognition Using LSTM
Speech is a rich and effective way of transmitting information among one another. Speech analysis can be of two types: linguistic and emotional. Virtual Personal Assistants like Siri and Alexa have attracted a remarkable amount of audience as a virtual helping hand to get things done quickly with ease. But still they lack the ability to analyse the emotional state and react according to that. This is why the need for emotion analysis arises. Through machine learning techniques, an effective model can be developed to predict emotions using the concept of Neural Networks.
This project aims to predict human emotions using LSTM (Long Short Term Memory). It is an aritficial Recurrent Neural Network architecture used in the firld of deep learning. An LSTM has feedback connections. It can, not only process single data points (such as images) but also entire sequences of data (such as audio or video).

# Datasets
On the route to develop an effective model to recognize the emotion of a particular speech segment, two existing datasets are combined and taken as base datasets. CREMA-D (Crowd Sourced Emotional Multimodal Actors Dataset) has 7,422 original clips from 91 actors while SAVEE (Survey Audio- Visual Expressed Emotion) has 480 audio files. The audio files in the datasets are classified among twelve categories as:
 1. Male Sad
 2. Male angry
 3. Male disgust
 4. Male fear
 5. Male happy
 6. Male neutral
 7. Female sad
 8. Female angry
 9. Female disgust
10. Female fear
11. Female happy 
12. Female neutral

The purpose of feature extraction is to analyse and compare the voice signals falling under these 12 categories. Speech analysis for both the genders is equally important due to the difference between amplitude in their voice. Samples from both the datasets are analysed based upon the frequency and amplitude. For example, when the speaker is angry, the amplitude of his/her voice is too high while it is generally too low when he/she is sad or depressed.

Datasets Link:

CREMA-D : https://www.kaggle.com/ejlok1/cremad

SAVEE   : https://www.kaggle.com/barelydedicated/savee-database

# Experimental Analysis 
A function evaluate_model() is defined that takes the train and test dataset, fits a model on the training dataset, evaluates it on the test dataset, and returns an estimate ofthe model’s performance. A single LSTM layer is used followed by a dropout layer with an intention of reducing over-fitting of the model to the training data. Then a dense fully connected layer is used to interpret the features extracted by the LSTM hidden layer, before a final output layer is used to make
predictions.
Two LSTM models are created using different loss functions. In Model 1 Categorical cross- entropy is used as the loss function, where as, in Model 2 Binary cross-entropy is used as the loss function. With Model 2 having higher accuracy as compared to that of Model 1, it is the best suited Model for the dataset. Binary cross-entropy is used for multi-label classifications, while categorical cross entropy on the other hand, is used for multi-class classification where each example belongs to a single class.   

# Testing
Model-2 came up with the maximum accuracy of 92.3%. So we tested it on a recorded sample of same dataset and found that the predictions were pretty accurate. This proves that the model-2 can be used in real life applications fro live speech extraction and emotion prediction.  
