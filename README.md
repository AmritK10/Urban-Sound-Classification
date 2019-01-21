# Urban-Sound-Classification

## Dataset
The UrbanSound8k dataset contains 8732 labeled sound excerpts (<=4s) of urban sounds from 10 classes: air_conditioner, car_horn, children_playing, dog_bark, drilling, enginge_idling, gun_shot, jackhammer, siren, and street_music. The classes are drawn from the urban sound taxonomy.All excerpts are taken from field recordings uploaded to www.freesound.org.<br/>
8732 audio files of urban sounds (see description above) in WAV format. The sampling rate, bit depth, and number of channels are the same as those of the original file uploaded to Freesound (and hence may vary from file to file).<br/>
The UrbanSound8k dataset used for model training, can be downloaded from the following link: https://urbansounddataset.weebly.com/ <br />

## Librosa
Librosa was used for data preprocessing and feature extraction.
Features used:<br/>
### MEL Features
#### MFCC <br/>
In sound processing, the mel-frequency cepstrum (MFC) is a representation of the short-term power spectrum of a sound, based on a linear cosine transform of a log power spectrum on a nonlinear mel scale of frequency.<br/>
Mel-frequency cepstral coefficients (MFCCs) are coefficients that collectively make up an MFC. They are derived from a type of cepstral representation of the audio clip (a nonlinear "spectrum-of-a-spectrum").<br/>
#### Melspectrogram <br/>
A mel-scaled spectrogram.
### Chroma Features
In music, the term chroma feature or chromagram closely relates to the twelve different pitch classes. Chroma-based features, which are also referred to as "pitch class profiles", are a powerful tool for analyzing music whose pitches can be meaningfully categorized (often into twelve categories) and whose tuning approximates to the equal-tempered scale. One main property of chroma features is that they capture harmonic and melodic characteristics of music, while being robust to changes in timbre and instrumentation.<br/>
#### Chroma_stft<br/>
A chromagram from a waveform or power spectrogram.<br/>
#### Chroma_cqt<br/>
Constant-Q chromagram.<br/>
#### Chroma_cens<br/>
The chroma variant “Chroma Energy Normalized” (CENS).<br/>
## Neural Network Implementation 
The following results are obtained by training on folders 1-9 and testing on folder 10. <br />
Train accuracy: 93.14% <br />
Test accuracy: 66.06%<br />

## Convolutional Neural Network Implementation 
The following results are obtained by training on folders 1-9 and testing on folder 10. <br />
Train accuracy: 95.90% <br />
Test accuracy: 73.11%<br />

