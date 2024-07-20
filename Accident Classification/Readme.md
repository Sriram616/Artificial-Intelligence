# Accident Detection from CCTV Footage using CNN

## Project Overview

This project involves detecting accidents from CCTV footage images using a Convolutional Neural Network (CNN). The dataset consists of images categorized into two classes: 'Accident' and 'Non-Accident'. The goal is to build, train, and evaluate a CNN model to accurately classify the images.

## Dataset

The dataset is organized into three directories:

- `train`: Training set images
- `test`: Test set images
- `val`: Validation set images

### Data Description

- **Image Size**: 256x256 pixels
- **Channels**: 3 (RGB)

## Code Overview

### Data Preparation

1. **Load Dataset**: Load the dataset from the specified directories using `tf.keras.preprocessing.image_dataset_from_directory`.
2. **Data Augmentation and Rescaling**: Apply resizing, rescaling, and data augmentation techniques to the images.

### Visualization

1. **Display Images**: Plot sample images from the dataset to verify data loading and labels.

### Model Building and Training

1. **CNN Model**:
   - **Architecture**: Multiple convolutional layers followed by max pooling, flattening, dropout, and dense layers.
   - **Compilation**: Optimized with Adam and trained using binary crossentropy loss.
   - **Training**: Trained for 25 epochs.

### Evaluation

1. **Model Evaluation**: Evaluate the model on the test dataset.
2. **Performance Metrics**: Plot training and validation accuracy and loss.

## Usage

1. **Run the Jupyter Notebook**: Execute the notebook to load data, build and train the model, and evaluate its performance.
2. **Visualize Results**: The notebook includes code to plot sample images and view model predictions.

## Results

- The model achieved satisfactory accuracy on the test set, demonstrating its capability to classify accident and non-accident images.

## Model Saving and Loading

- The trained model is saved as `accident_detection.h5` and can be loaded for future predictions.
