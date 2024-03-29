# Urban-Sound-Classification

## [Web App Repo](https://github.com/AmritK10/Urban-Sound-Classification-Webapp)

## References

Salamon, J., & Bello, J. P. (2017). Deep convolutional neural networks and data augmentation for environmental sound classification. IEEE Signal processing letters, 24(3), 279-283. https://doi.org/10.1109/LSP.2017.2657381

## Dataset

The UrbanSound8k dataset contains 8732 labeled sound excerpts (<=4s) of urban sounds from 10 classes: air_conditioner, car_horn, children_playing, dog_bark, drilling, enginge_idling, gun_shot, jackhammer, siren, and street_music. The classes are drawn from the urban sound taxonomy.All excerpts are taken from field recordings uploaded to www.freesound.org.<br/>
8732 audio files of urban sounds (see description above) in WAV format. The sampling rate, bit depth, and number of channels are the same as those of the original file uploaded to Freesound (and hence may vary from file to file).<br/>
The UrbanSound8k dataset used for model training, can be downloaded from the following link: https://urbansounddataset.weebly.com/ <br />

## Directory Structure

<i>Urban_data_preprocess.ipynb</i>: Pre-processing data and also augmenting data

<i>Urban_nn_model.ipynb</i>: Running 10 fold cross val on original data using simple NN

<i>Urban_cnn_model.ipynb</i>: Running 10 fold cross val on original and augmented data using CNN

<i>Urban_data_generator.ipynb</i>: Contains code for a data-generator that can be used for training with augmented data using CNN

## Results

10 Fold Cross Val Accuracy for NN using original data: 57.43% <br/>
10 Fold Cross Val Accuracy for CNN using original data: 62.61% <br/>
10 Fold Cross Val Accuracy for CNN using augmented data: 63.90% <br/>

## Future Work

Extend data more by using different parameters for augmentation <br/>
Apply Hyperparameter optimization and test different architectures <br/>

## Features Extracted

Librosa was used for data preprocessing and feature extraction.<br/>

### MEL Features

#### MFCC <br/>

In sound processing, the mel-frequency cepstrum (MFC) is a representation of the short-term power spectrum of a sound, based on a linear cosine transform of a log power spectrum on a nonlinear mel scale of frequency.<br/>
Mel-frequency cepstral coefficients (MFCCs) are coefficients that collectively make up an MFC. They are derived from a type of cepstral representation of the audio clip (a nonlinear "spectrum-of-a-spectrum").<br/>

#### MFCC of a dog bark<br/>

![image](https://user-images.githubusercontent.com/31596604/51472544-ce520c80-1d9f-11e9-883c-e08c4463a5b4.png)<br/>

#### Melspectrogram <br/>

A mel-scaled spectrogram.<br/>

#### Melspectrogram of a dog bark<br/>

![image](https://user-images.githubusercontent.com/31596604/51472743-5f28e800-1da0-11e9-9402-5ba41dfefae5.png)<br/>

### Chroma Features

In music, the term chroma feature or chromagram closely relates to the twelve different pitch classes. Chroma-based features, which are also referred to as "pitch class profiles", are a powerful tool for analyzing music whose pitches can be meaningfully categorized (often into twelve categories) and whose tuning approximates to the equal-tempered scale. One main property of chroma features is that they capture harmonic and melodic characteristics of music, while being robust to changes in timbre and instrumentation.<br/>

#### Chroma_stft<br/>

A chromagram from a waveform or power spectrogram.<br/>

#### Chromagram of a dog bark<br/>

![image](https://user-images.githubusercontent.com/31596604/51472838-a616dd80-1da0-11e9-87f3-54a6a9e03170.png)<br/>

#### Chroma_cqt<br/>

Constant-Q chromagram.<br/>

#### Constant-Q chromagram of a dog bark<br/>

![image](https://user-images.githubusercontent.com/31596604/51472906-e0807a80-1da0-11e9-8988-f060eed38957.png)<br/>

#### Chroma_cens<br/>

The chroma variant “Chroma Energy Normalized” (CENS).<br/>

#### Chroma cens of a dog bark<br/>

![image](https://user-images.githubusercontent.com/31596604/51472963-09087480-1da1-11e9-863f-084b84ecd584.png)<br/>
