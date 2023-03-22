# Sign_Language_Detection

this is a two-man research projects for the final year in Chinese Culture University CSE before graduation, sharing credits with @gary23897793@gmail.com.
The main goal of this project is to build a artificial intelligence (or AI for short), that can detect a person's sign language and recognize it, then print the meaning of the hand gesture on the screen 

this project will base on Python,
using Mediapipe to extract the keypoints of hand, face and body to achieve active recognition, then we will build up a LSTM deep learning model with Tensorflow and Keras to predict the sign language. Combine all together, print the result on the screen by opencv.


How it work
1. collecting data from different keypoints, saving in numpy arrays
2. train a deep neuro network using LSTM layers
3. perform real time detection using opencv

