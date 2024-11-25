# Face Detection using Support Vector Machine
This repository provides scripts for creating a custom face detection system without using pre-trained models. The approach leverages Histogram of Oriented Gradients (HOG) features for object detection, along with data augmentation, sliding windows, non-maximum suppression, FLAML library and  Support Vector Machines (SVM) classification.

## Approach Overview
### Data Loading and Augmentation:
Positive and negative image samples are loaded, respectively.
Positive images are augmented by simulating distance variation and adding mirrored images to increase training data.
Negative images are augmented by extracting random patches to diversify the negative dataset.

### Feature Extraction and SVM Training:
HOG features are extracted from both positive and augmented negative images.
An SVM classifier is trained using the positive and augmented negative features.
The best hyperparameters of SVM classifier model are evaluated by FLAML library.

### Object Detection:
The trained SVM model is used for detecting faces in test images.
A sliding window approach is employed to generate image patches for detection.
Non-maximum suppression is applied to remove redundant bounding boxes and improve detection accuracy.
