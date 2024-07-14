# Handwritten Digit Classification

## Project Overview

This project involves classifying handwritten digits using the MNIST dataset. The goal is to build a neural network model to recognize digits from 0 to 9 based on image data. The project demonstrates the use of TensorFlow and Keras for building and training the model.

## Dataset

The dataset used in this project is the MNIST dataset, which consists of 70,000 grayscale images of handwritten digits (0-9). The dataset is split into 60,000 training images and 10,000 test images.

### Dataset Description

- **Training Images**: 60,000 grayscale images of size 28x28 pixels.
- **Test Images**: 10,000 grayscale images of size 28x28 pixels.
- **Labels**: Each image is labeled with a digit from 0 to 9.

## Code Overview

### Data Preparation

1. **Load Data**: Load the MNIST dataset using Keras.
2. **Normalize Images**: Scale pixel values from [0, 255] to [0, 1].
3. **Flatten Images**: Reshape images from 28x28 to a 784-dimensional vector.

### Model Building and Training

1. **Initial Model**:
   - **Architecture**: Single dense layer with 10 units and sigmoid activation.
   - **Compilation**: Compiled with Adam optimizer and sparse categorical crossentropy loss.
   - **Training**: Trained for 5 epochs.

2. **Enhanced Model**:
   - **Architecture**: Added a hidden dense layer with 1000 units and ReLU activation, followed by an output layer with 10 units and softmax activation.
   - **Compilation**: Same as the initial model.
   - **Training**: Trained for 5 epochs.

### Model Evaluation

1. **Evaluation**: Assessed the model's performance on the test set.
2. **Predictions**: Generated predictions for test images and compared them to actual labels.

## Usage

1. **Run the Jupyter Notebook**: Execute the notebook to preprocess data, build and train the model, and evaluate its performance.
2. **View Results**: The notebook includes code to visualize example images and model predictions.

## Results

- The initial model with a single dense layer achieved basic accuracy on the test set.
- The enhanced model with an additional hidden layer showed improved performance.
