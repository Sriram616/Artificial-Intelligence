# Bangalore House Price Prediction

## Project Overview

This project aims to predict house prices in Bangalore using various features such as location, size, total square footage, number of bathrooms, and BHK (number of bedrooms, halls, and kitchens). The dataset is preprocessed to handle missing values, outliers, and categorical variables. Multiple regression models are tested to find the best one for price prediction.

## Dataset

The dataset contains information about various houses in Bangalore, including:

- **area_type**: Type of area (e.g., Super built-up Area, Plot Area, etc.)
- **availability**: When the property is available (e.g., Ready To Move, Immediate Possession, etc.)
- **location**: Location of the property
- **size**: Number of bedrooms (BHK)
- **society**: Name of the society
- **total_sqft**: Total area of the property in square feet
- **bath**: Number of bathrooms
- **balcony**: Number of balconies
- **price**: Price of the property in lakhs

## Code Overview

### Data Preparation

1. **Load Dataset**: The dataset is loaded from a CSV file.
2. **Drop Irrelevant Columns**: Columns such as 'area_type', 'society', 'balcony', and 'availability' are dropped.
3. **Handle Missing Values**: Rows with missing values are dropped.
4. **Feature Engineering**:
    - Extract the number of BHK from the 'size' column.
    - Convert 'total_sqft' to a numeric value, handling ranges and other formats.
    - Create a new feature 'price_per_sqft'.
5. **Location Normalization**: Normalize location names and group locations with less than 10 data points into 'other'.
6. **Outlier Removal**:
    - Remove outliers based on 'total_sqft' per BHK.
    - Remove outliers based on 'price_per_sqft'.
    - Remove properties with a disproportionate number of bathrooms.

### Model Building

1. **Train-Test Split**: Split the data into training and testing sets.
2. **Linear Regression Model**: Train a linear regression model.
3. **Cross-Validation**: Use cross-validation to evaluate the model's performance.
4. **Grid Search**: Use GridSearchCV to find the best model and hyperparameters among linear regression, lasso, and decision tree regressor.

### Prediction Function

- **predict_price**: A function that predicts the price of a house given the location, total square footage, number of bathrooms, and BHK.

### Model Saving

- The trained model is saved using pickle.
- The columns used in the model are saved in a JSON file.

## Usage

1. **Run the Jupyter Notebook**: Execute the notebook to load data, preprocess it, build and train the model, and evaluate its performance.
2. **Predict House Prices**: Use the `predict_price` function to predict house prices for given input features.

## Results

- The best model is selected based on cross-validation and grid search results.
- The model's performance metrics are evaluated and visualized.
