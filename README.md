<br />
<p align="center">
  <h3 align="center">Communities and Violent Crime</h3>

  <p align="center">
    Tested and optimized 6 varieties of supervised learning models to predict the rate of violent crime per 100K residents of U.S. communities based on community attributes. Used 122 community characteristics as features, drawn from U.S. Census data, the annual U.S. LEMAS (law enforcement) survey, and the FBI's UCR.  Useful wherever single-word spoken commands must be understood by devices or smart objects including autonomous vehicles.
    <br />
    <br />
    <a href="https://colab.research.google.com/drive/1Jr4WnqwSiqNEGMnRRoMf6Z5JTx6uOMty?usp=sharing">View Notebook</a>
  </p>
</p>


<!-- ABOUT THE PROJECT -->
## About The Project

I chose to tackle this project because of my ongoing interest in audio information retrieval and my desire to learn the Librosa Python library.


### Built With

* []() TensorFlow/Keras
* []() Librosa
* []() Numpy
* []() <a href="https://ai.googleblog.com/2017/08/launching-speech-commands-dataset.html">Audio data</a> from the Google AIY and TensorFlow teams


## Feature Engineering

The dataset consisted of 104,000 crowdsourced audio files of single-word spoken commands.  Two datasets were derived from this: one, the audio data itself, resampled to 8000 Hz and all samples shorter than 1 second dropped.  The second consists of an array of MFCCs (Mel frequency cepstrum coefficients) extracted from each audio file.  Each dataset was fed into a series of models, with the hypothesis that MFCCs would produce results almost as accurate and less computationally demanding than models requiring the full audio data.


## Model Building

Three basic structures for neural networks were based on research by data scientists at University of Montreal, Stanford, Cornell, and independent professionals.  These were then optimized methodically for a total of 16 models; the summary of these models can be found <a href="https://docs.google.com/spreadsheets/d/14gmZQ5KOuHXWG56O5N_PXGECjSVSUjJr0C5NGMiOcT8/edit?usp=sharing">here</a>.

The favored model has a training accuracy of 84% and testing accuracy of 83%, avoiding overfitting, and only requires MFCCs as input, resulting in a simpler, more computationally effective model than that used by the University of Montreal researchers and with higher accuracy.  The model has high precision and recall for all 34 of the labels identified.  Pairs of words most often (but still not often) confused by the model include: three/tree, go/no, four/forward, and up/off.


## Future Work

The next steps including combining RNNs with CNN layers effectively as some models have successfully done, adding audio features to MFCCs that may increase accuracy while not dramatically increasing training time, and considering either adding or eliminating background noise to the audio samples.
