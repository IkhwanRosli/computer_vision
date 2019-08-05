# Face Detection
This is the fundamental knowledge we need to know before we can proceed to face recognition, gender detection or age detection. Usually, people using OpenCV Haar Cascades to do face detection. However, for this code, I'm using the resnet model to received higher accuracy when doing the detection. There are 2 codes in this project which one for doing face detection on images and the other one for real-time detection.

I will explained a bit about my code.

### Face Detection on Image
The library we need for this are NumPy, OpenCV and Argparse.\
'''python
import numpy as np
import argparse
import cv2
'''

Argparse module were used to makes it easy to write user friendly command-line interfaces.\
'''pythoap = argparse.ArgumentParser()
ap.add_argument("-i","--image", required = True, help="path to input image")
ap.add_argument("-p","--prototxt", required = True, help="path to Caffe 'deploy' prototxt file")
ap.add_argument("-m","--model", required = True, help="path to Caffe pre-trained model")
ap.add_argument("-c","--confidence", type=float, default=0.5, help="minimum probability to filter weak detections")
args = vars(ap.parse_args())
'''


