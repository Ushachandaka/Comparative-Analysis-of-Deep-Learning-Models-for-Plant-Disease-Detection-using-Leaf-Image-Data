# Comparative-Analysis-of-Deep-Learning-Models-for-Plant-Disease-Detection-using-Leaf-Image-Data
This project presents a comparative analysis of deep learning models for plant disease detection using leaf image datasets. It evaluates models such as CNN, ResNet, VGG16, and MobileNet based on accuracy, precision, recall, training time, and efficiency to identify the most effective approach for early and reliable plant disease classification.

#Plant Disease Detection using Deep Learning

This project focuses on the classification of plant diseases using deep learning techniques on leaf image data from the PlantVillage Dataset. The aim is to compare the performance of a baseline Convolutional Neural Network (CNN) model with a transfer learning approach using MobileNetV2.

#Project Objective

The objective of this project is to identify plant diseases from leaf images and evaluate which deep learning model performs better for image classification tasks.

#Dataset

The project uses a reduced version of the PlantVillage dataset containing selected classes such as:

Tomato Healthy
Tomato Late Blight
Potato Early Blight
Potato Healthy

To reduce training time and computational requirements, a limited number of images per class were selected.

#Preprocessing Steps

The following preprocessing techniques were applied:

Image resizing to 224×224
Pixel normalization using rescaling
Train-validation split (80%-20%)
Data augmentation:
Rotation
Zoom
Horizontal flipping
