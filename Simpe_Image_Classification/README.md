# Image Classification with CNN

## Project Overview

This project involves classifying images from the CIFAR-10 dataset using a Convolutional Neural Network (CNN). The dataset consists of 60,000 32x32 color images in 10 different classes. The goal is to build and evaluate both a simple artificial neural network (ANN) and a CNN for image classification.

## Dataset

The CIFAR-10 dataset contains 60,000 32x32 color images categorized into 10 classes:

- **Classes**: ['airplane', 'automobile', 'bird', 'cat', 'deer', 'dog', 'frog', 'horse', 'ship', 'truck']

### Data Description

- **Training Images**: 50,000 images
- **Test Images**: 10,000 images
- **Image Size**: 32x32 pixels
- **Channels**: 3 (RGB)

## Code Overview

### Data Preparation

1. **Load Dataset**: Load CIFAR-10 dataset using TensorFlow/Keras.
2. **Reshape Labels**: Reshape the labels to a 1D array.
3. **Scale Images**: Normalize pixel values from [0, 255] to [0, 1].

### Visualization

1. **Display Images**: Plot sample images from the dataset to verify data loading and labels.

### Model Building and Training

1. **Artificial Neural Network (ANN)**:
   - **Architecture**: Flattened input with two dense layers followed by an output layer.
   - **Compilation**: Optimized with SGD and trained using sparse categorical crossentropy loss.
   - **Training**: Trained for 5 epochs.

2. **Convolutional Neural Network (CNN)**:
   - **Architecture**: Convolutional layers followed by max pooling, flattening, and dense layers.
   - **Compilation**: Optimized with Adam and trained using sparse categorical crossentropy loss.
   - **Training**: Trained for 10 epochs.

### Evaluation

1. **ANN**:
   - **Model Evaluation**: Evaluate the model on the test dataset.
   - **Classification Report**: Generate and print the classification report.

2. **CNN**:
   - **Model Evaluation**: Evaluate the CNN on the test dataset.
   - **Classification Report**: Generate and print the classification report.

## Usage

1. **Run the Jupyter Notebook**: Execute the notebook to load data, build and train models, and evaluate their performance.
2. **Visualize Results**: The notebook includes code to plot sample images and view model predictions.

## Results

- The ANN model provided a baseline performance.
- The CNN model, with its convolutional layers, achieved better accuracy and performance metrics.
