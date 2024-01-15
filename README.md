# Sign Language Detection

this is a two-man research projects for the final year in Chinese Culture University CSE before graduation, sharing credits with @gary23897793@gmail.com.
The main goal of this project is to build a artificial intelligence (or AI for short) that can detect a person's sign language and recognize it, then print the meaning of the hand gesture on the screen 

Hand gestures are all based on TSL(Taiwan Sign Language) 

this project will be base on Python,
using Mediapipe to extract the keypoints of hand, face and body to achieve active recognition, then we will build up a CNN and LSTM deep learning model with Tensorflow and Keras to predict the sign language. Combine all together, print the result on the screen by opencv.

How it work
1. collecting data from different keypoints, paint on a size of 150*150 all 0 numpy array
2. train a deep neuro network using TimedistributedCNN and LSTM layers
3. perform real time detection using opencv

## Collecting Data

Existing database which support or based on TSL are super hard to find, although in Taiwan you can find a proper tutorial video and website that teach you proper Taiwan sign language, a huge amount of data of sign language still almost don't opened online.

The Straightest way is just record the frame by our own.

After our testing, we've chosen 45 frame to be in our single observation. 45 frame can completely record a gesture from start to end.

Of course, if you want to record your own data, the number of frame is adjustable, it's 45 just because it fit our poor camera the best.

some points need to be caution:
- in this project, recording videos require a camera.
- in our experiment, drastically quick moving or environment brightness will cause Mediapipe keypoint disappear. This will make some of the     frame in single video become useless. So, we implement a function to detect if there exist any frame lacking keypoints. Any lacking keypoints frame will automatically redo the current video recording. In some kind of situation, this will be very irritating and annoying, but it can help us to maintain data integrity.

if you are interest in the whole file, here are the links: 
https://drive.google.com/file/d/1wfubFCg_XC5zDYnWojsZYZjevAQOzHFC/view?usp=sharing

---
I know, this is not perfect, still need a lot of optimization. But in the process of researching this topic, we learned lots of skill about image process and deep learning. 

Hope this not perfect project can inspired someone in the future.

If you have any question or issue, feel free to contact me. 
Lu Shang Hung(or Jason Lu): sunwasd456@gmal.com
