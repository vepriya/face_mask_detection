# face_mask_detection
### This repository contains the source code of face mask detector using opencv and keras

# Dataset
face_mask dataset contains 5000 images.\
dataset:\
with_mask(2500 images)\
without_mask(2500 images)

# Taining
![alt tag](https://github.com/vepriya/face_mask_detection/blob/master/face_mask_detection_phases.png)

trained the fask_mask_detector in two phases:
### phase1:
1. Load the face mask dataset(which contains images of only faces with and without mask) and  train fasce_mask_classifier with the help    of tensorflow and keras.
2. Fine tunned a MobileNetV2 with new fresh fully connected head to build the classifier model and trained on dataset.

### phase2
1. We will use opencv pretrained face detector from the opencv dnn module to detect the faces in input images.
2. Download the .prototxt and .caffemodel file from the https://github.com/opencv/opencv/tree/master/samples/dnn face detector.
3. After detecting faces in image we will aplly our face mask classifier to each face  detected by face detector and face mask      classifier will classifiy whether the person is wearing mask or not

# Prediction
1 .To predict whether the person is wearing mask or not in a image run detect_mask_image.py and pass the input image in command line for    example:- python detect_mask_image_py --image example_01.png \
2. To predict whether the person is wearing mask or not in a video run detect_mask_video.py
