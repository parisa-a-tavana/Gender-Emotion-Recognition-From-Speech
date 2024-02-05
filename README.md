# Gender-Emotion-Recognition-From-Speech
In this project we impliment different machine learning methods to classify speech based on gender and emotion of the speakers.
<br>
<br>
**Data Set**:
<br>
We record 400 people (men and women) reading 10 different sentences in 4 emotions: sad, happy, angry, and neutral. Each audio sample has 2 labels:
<br>
Emotion ID: {1 : 'Angry', 2 : 'Happy', 3 : 'Sad', 4 : 'Neutral'}
Gender ID: {0: 'male' , 1: 'female'}

<br>
<br>
**Feature Extraction**:
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
<br>





