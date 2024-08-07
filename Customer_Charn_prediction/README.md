# Customer Churn Prediction

## Project Overview

This project involves predicting customer churn using a dataset from a telecom company. The goal is to classify whether a customer will churn (leave) or not based on various features such as tenure, monthly charges, and service usage.

## Dataset

The dataset used in this project includes customer-related features and a target variable indicating whether the customer has churned.

### Dataset Description

- **customerID**: Unique ID for each customer.
- **tenure**: Number of months the customer has been with the company.
- **MonthlyCharges**: Monthly charges for the customer.
- **TotalCharges**: Total charges incurred by the customer.
- **Churn**: Whether the customer has churned or not (target variable).
- **Other features**: Various service-related features.

## Code Overview

### Data Preprocessing

1. **Load Data**:
   - Load the CSV file into a DataFrame.

2. **Data Cleaning**:
   - Remove unnecessary columns.
   - Handle missing values and data types.

3. **Feature Engineering**:
   - Encode categorical variables.
   - Scale numerical features.

4. **Prepare Data for Training**:
   - Split data into training and testing sets.

### Model Building and Training

1. **Build the Model**:
   - Define a simple neural network with TensorFlow/Keras.

2. **Compile the Model**:
   - Use `adam` optimizer and `binary_crossentropy` loss function.

3. **Train the Model**:
   - Fit the model on the training data.

4. **Evaluate the Model**:
   - Assess the model's performance on the test data.

5. **Predict and Evaluate**:
   - Generate predictions and compare with actual values.

## Usage

Run the Jupyter notebook or Python script to perform the following actions:

1. Load and preprocess the data.
2. Train the model.
3. Evaluate the model's performance.

## Results

The model's performance metrics are displayed after training. Predictions on test data are also provided.
