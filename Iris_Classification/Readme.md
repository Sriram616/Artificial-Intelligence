# Iris Classification

## Project Overview

This project involves classifying the species of iris flowers based on their sepal and petal measurements using machine learning algorithms. The dataset used is the famous Iris dataset, which contains 150 samples of iris flowers with four features each: sepal length, sepal width, petal length, and petal width. There are three species of iris flowers in the dataset: Setosa, Versicolour, and Virginica.

## Dataset

The Iris dataset contains the following features:

- **sepal length (cm)**
- **sepal width (cm)**
- **petal length (cm)**
- **petal width (cm)**
- **target**: The species of the iris flower (0: Setosa, 1: Versicolour, 2: Virginica)

## Code Overview

### Data Loading and Preparation

1. **Load Dataset**: The dataset is loaded using the `load_iris` function from `sklearn.datasets`.
2. **Create DataFrame**: A DataFrame is created from the dataset for easier manipulation and analysis.
3. **Add Target and Flower Name**: The target values and corresponding flower names are added to the DataFrame.

### Data Visualization

- **Scatter Plots**: Scatter plots are created to visualize the relationships between the different features of the dataset.

### Model Building

1. **Train-Test Split**: The dataset is split into training and testing sets.
2. **Support Vector Machine (SVM) Model**: An SVM model is trained on the training data.
3. **Model Evaluation**: The accuracy of the model is evaluated on the test data.

### Results

- The accuracy score of the SVM model is printed to evaluate its performance.
