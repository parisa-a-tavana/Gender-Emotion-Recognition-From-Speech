# Gender-Emotion-Recognition-From-Speech
In this project we impliment different machine learning methods to classify speech based on gender and emotion of the speakers.
<br>
<br>
**Data Set**:
<br>
We record 400 people (men and women) reading 10 different sentences in 4 emotions: sad, happy, angry, and neutral. Each audio sample has 2 labels:
<br>
Emotion ID: {1 : 'Angry', 2 : 'Happy', 3 : 'Sad', 4 : 'Neutral'}
<br>
Gender ID: {0: 'male' , 1: 'female}
<br>
We use the noisereduce library to remove noise from the audio samples.
<br>
We also shuffle and split the data set into train and test data.
<br>
<br>
__Feature Extraction__:
<br>
We frist extrat the features below using the librosa library.
<br>
Mel  Frequency Coefficients Cepstral (MFCC): They represent the logarithmically spaced frequency bands of the signal and capture characteristics of the audio signal relevant to human auditory perception.
<br>
Chroma Frequencies: They represent the twelve pitch classes in music, capturing the tonal characteristics of audio. They condense musical information by focusing on the presence of pitch classes, commonly used for tasks like chord recognition and genre classification.
<br>
Spectral Rolloff: It represents the frequency below which a certain percentage of the total spectral energy lies and helps characterize the high-frequency content of a signal.
<br>
Spectral Centroid: It indicates the "center of mass" of the frequency content in a sound spectrum and provides a measure of the average frequency and is often used to characterize the tonal center or brightness of a sound.
<br>
Zero Crossing: It counts the number of times the audio waveform crosses the zero amplitude axis and is used to characterize the rate of changes in the signal. 
<br>
After extracting the features, we use MinMaxScaler from scikit-learn to transform features to the same range.
<br>
<br>
__Classificatin__:
<br>
We employ 4 distinct classification models: MLP, KNN, SVM, and Logistic Regression. For each model, one is dedicated to gender classification, and another is assigned to emotion classification, resulting in a total of 8 models. Using cross-validation, we determine optimal hyperparameters for each model, selecting parameters based on accuracy. Following the identification of the best hyperparameters for each model, we proceed to train them on the training dataset and evaluate their performance on the test dataset.
<br>
Here is the comparison of models' accuracy: 
<br>
![Alt text](images/accuracy.png)
![Alt text](images/confusion emotion.png)
![Alt text](images/confusion gender.png)
![Alt text](images/roc emotion.png)
![Alt text](images/roc gender.png)








