## *stanCode* SC201 Project - Music Emotion Prediction :clipboard:
Hello there!\
This repository holds Music Emotion Prediction project done during the period of stanCode SC201 course.


### :pushpin: Project Objective:

  Music plays an important role in affecting our mood. When we are sad, we might feel like listening to songs that could cheer us up. When we are angry, we might want a smoothing song which could make us calm down. In order to select a specific song that would trigger specific feelings, classifying perceived emotion when people listening to a track could be useful. Therefore, this project aims to develop a deep learning model to automatically determining the values of features (i.e., arousal and valence) associated with perceived emotion during the process of people listening to a track. We hope this project can facilitate future music emotion recognition work.

### :pushpin: Project Dataset:

  Our main focus is on predicting a song’s perceived emotion features (i.e., arousal and valence) using acoustic features associated with a song every 10 second. Thus, we treat dynamic emotion features as our target labels and dynamic acoustic features as out input data.
The dataset we are using is PMEmo Dataset from The PMEmo Dataset for Music Emotion Recognition (Zhang et al., [2018](https://dl.acm.org/doi/10.1145/3206025.3206037)).
If you would like to glance the whole PMEmo dataset and detailed description of it, you could click the above link to the paper. And after that, if you would like to save space, you could simply download the required files for this project from [here](https://drive.google.com/drive/folders/1JqynbSCXSBRhln9YsHI72FSYHPlTkadl?usp=share_link). 

### :pushpin: Project Approaches:

  To deal with a sequence of input data and a sequence of target labels, we build up two models - Bidirectional LSTM Model and Transformer Encoder Model - to train separately with Adam as optimizer and mean square error as our loss function. After finishing training and validation for hyper-parameter tuning, we test a trained model with acoustic features and then predict emotion features using the trained model with tuned hyper-parameters. 

  The `model_to_train` variable can be used to decide which model is to be trained. If assigning `”BiLSTM”` to the variable, Bidirectional LSTM Model will be trained. If assigning `”TransformerEncoder”` to the variable, Transformer Encoder Model will be trained.

### :pushpin: Project Execution:

   To see the training, validating, testing and predicting process,
1. Create a folder and name it music_emotion_prediction_project under Colab Notebooks folder on your google drive.
2. Create a folder and name it raw_dataset under music_emotion_prediction_project folder which is created in the first step.
3. Create a folder and name it plots under music_emotion_prediction_project folder on your google drive.
4. Upload two needed files and place them in a raw_dataset folder on your google drive. 
5. Upload [music_emotion_prediction.ipynb](https://github.com/CharleneChar/stanCodeSC201Projects/blob/main/music_emotion_prediction.ipynb) and place it under music_emotion_prediction_project folder on your google drive
6. Execute music_emotion_prediction.ipynb on Google Colab

  Here is the quick result after executing this project:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/CharleneChar/stanCodeSC201Projects/blob/main/music_emotion_prediction.ipynb)

### :pushpin: Project Source Code:
  * [Music Emotion Prediction](https://github.com/CharleneChar/stanCodeSC201Projects/blob/main/music_emotion_prediction.ipynb)

### :pushpin: Project Future Work:

  With better interpretability, unsupervised learning like k-means clustering can be applied to the predicted valence and arousal values from our project to further classify perceived emotions such as happy, sad, and so on when listening to a track.
