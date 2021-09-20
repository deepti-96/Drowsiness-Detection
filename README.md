# Drowsiness Detection


## Introduction

A computer vision system based on opencv that monitors a video stream for driver drowsiness and plays an alarm if the driver appears to be sleepy.

## Code Requirements

Python is the programming language used in the example code (version 2.7 and higher will work).

## Dependencies

 1. import cv2</br>
 2. import immutils</br>
 3. import dlib</br>
 4. import scipy</br>
 5. import playsound</br>
 6. import queue</br>
 7. import time</br>
 8. import sys</br>

## Algorithm
● Based on a modification to the Histogram of Oriented Gradients, we used Linear SVM for classification in combination with a pre-trained frontal face detector from Dlib's library. </br>
● The pre-trained facial landmark detector in the dlib library is used to estimate the position of 68 (x, y)-coordinates that correspond to facial structures on the face. The following figure illustrates the 68 landmark output. We used the 70 landmark model, however.</br>
 
 ![image](https://user-images.githubusercontent.com/72935128/134086917-d7d86a4c-1da7-43b4-b681-8b24d615b9a5.png)

● The aspect ratio is then calculated to see if the eyes are open or closed.</br>
● If the Eye Aspect Ratio is larger than a threshold, the eye is open. (Roughly 0.3)</br>
 
 ![image](https://user-images.githubusercontent.com/72935128/134086896-1a6a801d-f3e5-4bd3-ad89-3afa3c4c963f.png)

● A blink should last between 200 and 300 milliseconds.</br>
● A sleepy blink would last 800-900 milliseconds.</br>

![eye_aspect_ratio](https://user-images.githubusercontent.com/72935128/134087408-e96058b8-67cd-49d6-a669-35168b5a8518.PNG)

## Application

It can be used by riders who tend to drive for longer periods, where drowsines could result in accidents. 


