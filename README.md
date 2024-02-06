# Gender-Emotion-Recognition-From-Speech
In this project we impliment different machine learning methods to classify speech based on gender and emotion of the speakers.
<br>
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
<br>
__Classificatin__:
<br>
We employ 4 distinct classification models: MLP, KNN, SVM, and Logistic Regression. For each model, one is dedicated to gender classification, and another is assigned to emotion classification, resulting in a total of 8 models. Using cross-validation, we determine optimal hyperparameters for each model, selecting parameters based on accuracy. Following the identification of the best hyperparameters for each model, we proceed to train them on the training dataset and evaluate their performance on the test dataset.
<br>
<br>
<br>
__Classification Results__: 
<br>
<br>
Models accuracy:
<br>
![Image 1](images/accuracy.png)
<br>
<br>
Emotion classification confusion matrices
<br>
![Image 2](images/confusion_emotion.png)
<br>
<br>
Gender classification matrices
<br>
![Image 3](images/confusion_gender.png)
<br>
<br>
Emotion classification ROC plot
<br>
![Image 4](images/roc_emotion.png)
<br>
<br>
Gender classification ROC plot
![Image 5](images/roc_gender.png)
<br>
<br>
<br>
__Clustering__:
<br>
We apply three clustering techniques: K-means, GMM clustering, and Agglomerative clustering. For each method, we group the data into 2, 4, and 10 clusters. We evaluate the quality of the clusterings using both supervised and unsupervised criterias:
<br>
Supervised criteria: Homogeneity, Mutual Information 
<br>
Unsupervised criteria: Silhouette , Davis Bouldin
<br>
To visualize the clusters effectively, we employ PCA to reduce the data's dimensions to two, capturing the most significant variance.
<br>
<br>
<br>
__Clustering Results__:
<br>
<br>
2 cluster evaluation:
<br>
![Image 6](images/cluster2.png)
<br>
<br>
4 cluster evaluation:
<br>
![Image 7](images/cluster4.png)
<br>
<br>
10 cluster evaluation:
<br>
![Image 8](images/cluster10.png)
<br>
<br>
Cluster visualisation:

<br>
![Image 9](images/all_clusters.png)









