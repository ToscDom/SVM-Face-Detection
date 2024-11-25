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

# References
1. https://medium.com/@mouse3mic3/a-practical-guide-to-automated-machine-learning-in-python-using-flaml-c73a714887a4

2. H. Chandra, ‘Pipelines & Custom Transformers in scikit-learn: The step-by-step guide (with Python code)’, Medium, Jun. 27, 2020. https://towardsdatascience.com/pipelines-custom-transformers-in-scikit-learn-the-step-by-step-guide-with-python-code-4a7d9b068156.

3. M. Tyagi, ‘HOG(Histogram of Oriented Gradients)’, Medium, Jul. 24, 2021. https://towardsdatascience.com/hog-histogram-of-oriented-gradients-67ecd887675f

4. N. Dalal and B. Triggs, ‘Histograms of oriented gradients for human detection’, in 2005 IEEE computer society conference on computer vision and pattern recognition (CVPR’05), Ieee, 2005, pp. 886–893.

5. C.-H. Yuan, ‘Face-Detection-with-a-Sliding-Window’. May 30, 2023. [Online]. Available: https://github.com/lionelmessi6410/Face-Detection-with-a-Sliding-Window

6. ‘Face Detection Project’. https://www.cc.gatech.edu/classes/AY2016/cs4476_fall/results/proj5/html/agartia3/index.html

7. J. Hosang, R. Benenson, and B. Schiele, ‘Learning non-maximum suppression’, in Proceedings of the IEEE conference on computer vision and pattern recognition, 2017, pp. 4507–4515.

8. "ProfAI: A Virtual Data Science Coach," ProfessionAI, 2023. Online. Available: https://prof.profession.ai/

9. “ChatGPT”. OpenAI's ChatGPT, 2023 - Conversational AI Language Model. [Online]. Available: https://chat.openai.com/

10) https://colab.research.google.com/drive/1H5jn1nzTA1Y0FpsbKEIZYoA3VoKPp_3Z?usp=sharing
