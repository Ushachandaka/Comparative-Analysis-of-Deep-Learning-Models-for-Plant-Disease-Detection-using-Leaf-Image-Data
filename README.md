# Comparative-Analysis-of-Deep-Learning-Models-for-Plant-Disease-Detection-using-Leaf-Image-Data
This project presents a comparative analysis of deep learning models for plant disease detection using leaf image datasets. It evaluates models such as CNN, ResNet, VGG16, and MobileNet based on accuracy, precision, recall, training time, and efficiency to identify the most effective approach for early and reliable plant disease classification.

# Plant Disease Detection using Deep Learning

This project focuses on the classification of plant diseases using deep learning techniques on leaf image data from the PlantVillage Dataset. The aim is to compare the performance of a baseline Convolutional Neural Network (CNN) model with a transfer learning approach using MobileNetV2.

# Project Objective

The objective of this project is to identify plant diseases from leaf images and evaluate which deep learning model performs better for image classification tasks.

# Dataset

# Dataset Structure

The project uses a customized subset of the PlantVillage dataset containing approximately 700 leaf images distributed across four classes:

PlantVillage_small/
├── Potato_early_blight
├── Potato_healthy
├── Tomato_healthy
└── Tomato_Late_blight

Each folder represents a unique class label. TensorFlow's flow_from_directory() automatically generates class labels from the folder names, simplifying dataset management and loading.

Dataset Split

The dataset was divided into:

Training Set: 80% (~600 images)
Validation Set: 20% (~150 images)

The split was performed automatically using:

validation_split=0.2

within TensorFlow's ImageDataGenerator.

# Data Preprocessing

Image preprocessing was performed to standardize the dataset and improve model performance.

1. Image Resizing

All images were resized to:

224 × 224 pixels

This input size is compatible with:

Convolutional Neural Networks (CNN)
MobileNetV2
EfficientNetB0
target_size = (224, 224)

Resizing ensures consistent input dimensions while preserving important disease-related features.

2. Pixel Normalization

Pixel values originally ranged from 0–255.

Normalization was applied by dividing pixel values by 255:

rescale=1./255

Resulting range:

0 ≤ Pixel Value ≤ 1

Benefits include:

Faster convergence
Improved numerical stability
Reduced gradient-related issues
Better optimization during training

# 3. Data Augmentation

To improve dataset diversity and reduce overfitting, several augmentation techniques were applied:

Technique	Parameter	Purpose
Rotation	rotation_range=20	Simulates different leaf orientations
Zoom	zoom_range=0.2	Improves scale invariance
Horizontal Flip	horizontal_flip=True	Generates additional image variations

These augmentations help the model generalize better to unseen data.

# 4. Data Loading

Images were loaded using TensorFlow's ImageDataGenerator.

Configuration:

batch_size = 32
class_mode = 'categorical'

Advantages:

Efficient memory usage
Real-time augmentation
Automatic label generation
Batch-wise processing
Exploratory Data Analysis (EDA)
Purpose

EDA was conducted to:

Verify image quality
Confirm successful preprocessing
Examine disease characteristics
Identify class balance issues
Understand visual differences between classes
Visual Inspection

Random samples from the training dataset were visualized using Matplotlib.

images, labels = next(train_data)

The inspection confirmed that:

Images were loaded correctly
Resizing was successful
Color information was preserved
Disease symptoms were clearly visible
Observed Disease Features
Color Variations

Disease symptoms produced noticeable color changes, including:

Yellow discoloration
Brown necrotic regions
White fungal growth

These color differences provide useful features for deep learning models.

Texture Differences

Diseased leaves often displayed:

Rough surfaces
Lesions
Irregular texture patterns

CNN-based models can automatically learn these texture characteristics.

Structural Changes

Certain diseases altered leaf morphology through:

Curling
Shrinking
Deformation

These structural variations provide additional information for classification.

<img width="794" height="690" alt="image" src="https://github.com/user-attachments/assets/ec6008fe-0bad-44bf-92fb-cfa8751f6027" />


