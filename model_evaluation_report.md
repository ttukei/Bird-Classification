## Summary

In this project, I developed a machine-learning model to classify 200 bird species from images in the CUB_200_2011 dataset. The model was built using the YOLOv7 architecture and trained from scratch.

This model shows a **mean average precision of 0.7–0.8** on the test set, indicating it has an ability to classify 200 birds from the dataset correctly. Also, it had a **F1 score of 0.75**, showing good balance between precision and recall.

Generally, the model performed well classifying 200 bird species sourced from the dataset, although there is always room for further improvement: data augmentation, more advanced architectures, maybe, could result in better performance such as classifying similar species more accurately.

## Introduction

Being able to classify bird species accurately falls under applications in ecology, monitoring of wildlife, and conservation. For example, volunteers participating in the Christmas Bird Count in Washington which is one of the longest-running citizen science projects in ornithology may be able to employ this technology through the use of an app increasing productivity and accuracy.

The project is based on a CUB_200_2011 dataset containing pictures of 200 species, totaling more than 11,000 annotated images.

The main objective was to create a machine-learning model that is able to classify images of bird species from a diverse group. This report goes over how the model was built, and evaluated, and key learnings together with possible further improvements that may provide better results.

## Methodology

### Dataset Preparation

The images in the CUB_200_2011 dataset were resized to 640x640 pixels to for the use of YOLOv7. Training and test sets were prepared with the help of metadata.

### Model Architecture

YOLOv7 is a real-time object detection model that boasts high accuracy and efficiency. It consists of three parts: the backbone, CSPDarknet53, for feature extraction; the neck, PANet, to enhance feature fusion; and the head, which predicts class labels, bounding box coordinates, and objectness scores. YOLOv7 is optimized for speed and accuracy, making it very suitable for applications like image classification.[^1.]

### Training Process

The model was trained with the following parameters: Batch Size: 16, Optimizer: Stochastic Gradient Descent (SGD), Learning Rate: Set in the configuration file, Epochs: 300.

Training was performed on a n1-standard-1 Google Cloud Virtual Machine with a 1 NVIDIA T4 GPU, and the model was trained from scratch.

## Conclusion

The YOLOv7 model has performed well in classifying bird species with strong accuracy. There's definitely room for further improvment.

[^1.][Ultralytics (2022)](https://docs.ultralytics.com/models/yolov7/?utm_source=chatgpt.com), "YOLOv7 Model Documentation."
