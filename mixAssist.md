## MIX ASSISTANT 

**Project description:** Mix Assistant is an application that will allow audio producers to gain insights into their audio 'mix' according to their individual listening preferences. Users will tell the application what song mixes they like, and Mix Assistant will save these preferences. Users will then be able to upload their own audio files for Mix Assistant to process and return tips and hints for the user to achieve their desired mix. 
<br>

**Step 1: Genre classification using the Spotify Web API**
<br>
I will be approaching this project through a pipeline of machine learning steps. The first is genre classification. There are often trends within a given genre, and there are often trends within a given users listening preferences. This use of the API was an effective learning experience for me. However, being that I do not actually have access the audio files themselves, and thus the Spectrograms or MFCCs, I was limited in what I could achieve. 

[ipynb File](pdf/SpotifyGenreClassifier.ipynb)
<br>
[Data Summary](images/SpotifyClassDescription.png?raw=true)

### Technologies 
<p>
 <a href="https://www.python.org">1. Python</a>
  <br>
 <a href="https://scikit-learn.org/stable/">2. Scikit-learn</a>
  <br>
 <a href="https://developer.spotify.com/dashboard/login">3. Spotify Web API</a>
  <br>
 <a href="https://www.scipy.org">4. SciPy</a> 
  <br>
 <a href="https://www.tableau.com">5. Tableau</a>  
  <br>
 <a href="https://colab.research.google.com/notebooks/intro.ipynb#recent=true">6. Google Colaboratory</a>   
  <br>
</p>  

<img src="images/SpotifyGenreClassConfusionMatrix.png?raw=true"/>
<img src="images/SpotifyGenreClassScores.png?raw=true"/>

**Step 2: Genre classification using the GTZAN Dataset**
<br>
With the GTZAN Dataset, downloaded from Kaggle, I was able to achieve over 70% accuracy across 9 genres (I had to remove Jazz). This provided me with an approach moving forward to classify genres once I have assembled my own dataset. This effectively introduced me to Convolutional Neural Networks and TensorFlow. 

### Technologies 
<p>
 <a href="https://www.python.org">1. Python</a>
  <br>
 <a href="https://scikit-learn.org/stable/">2. Scikit-learn</a>
  <br>
 <a href="https://www.tensorflow.org">3. TensorFlow</a>
  <br>
 <a href="https://matplotlib.org">4. Matplotlib</a> 
  <br>
  <a href="https://numpy.org">5. NumPy</a> 
  <br>
</p> 

<img src="images/CNN_GTZAN.png?raw=true"/>

**Step 3: Setting up a basic application for importing audio files and running the classification**
<br>
Currently I am working to build an application within SwiftUI to allow users to upload audio files for processing. The current challenge is dealing with Uniform Type Identifiers and running Python Scripts within the app. Below is a screen shot of the general idea for file uploads. 

<img src="images/MixAssistFileUpload.png?raw=true"/>
