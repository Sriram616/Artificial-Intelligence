# Bengaluru House Price Prediction

## Project Overview

This project aims to predict house prices in Bengaluru using various regression techniques. The dataset consists of features like location, size, total square feet, number of bathrooms, and more.

## Dataset

The dataset used in this project is `Bengaluru_House_Data.csv`, which contains the following columns:

- `area_type`
- `availability`
- `location`
- `size`
- `society`
- `total_sqft`
- `bath`
- `balcony`
- `price`

### Data Cleaning and Preprocessing

1. **Handling Missing Values**: Dropped columns with too many missing values and rows with null values.
2. **Feature Engineering**:
   - Extracted BHK (number of bedrooms) from the `size` column.
   - Converted total square feet to a numeric format.
   - Created a new feature `price_per_sqft`.
3. **Dimensionality Reduction**: Grouped locations with less than 10 occurrences into an 'other' category.
4. **Outlier Removal**:
   - Removed outliers based on the `total_sqft` per BHK.
   - Removed properties with an unusually high number of bathrooms.
   - Removed properties with `price_per_sqft` outliers.

### Visualization

- Scatter plots to visualize the relationship between total square feet and price.
- Histograms for price per square feet and number of bathrooms.

## Model Building

### Algorithms Used

1. **Linear Regression**: Baseline model.
2. **Lasso Regression**: For feature selection.
3. **Decision Tree Regression**: For non-linear relationships.

### Model Evaluation

- Used k-fold cross-validation to evaluate model performance.
- Compared models using GridSearchCV to find the best parameters.

### Results

- Linear Regression was chosen as the final model based on cross-validation results.

## Usage

### Prerequisites

- Python 3.x
- Pandas
- Numpy
- Matplotlib
- Scikit-learn
- TensorFlow
- Keras
- Google Colab (for running the notebook)
- Kaggle (for accessing the dataset)

### Running the Project

1. **Clone the Repository**:
    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```
2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
3. **Run the Jupyter Notebook**:
    Open and run the `ML_PRJT_.ipynb` notebook in Jupyter or Google Colab.

### Predicting House Prices

To predict house prices using the trained model:
1. Load the saved model:
    ```python
    import pickle
    with open('banglore_home_price_prediction_model.pickle', 'rb') as f:
        model = pickle.load(f)
    ```
2. Predict the price:
    ```python
    def predict_price(location, sqft, bath, bhk):
        global X
        loc_index = np.where(X.columns == location)[0][0]

        x = np.zeros(len(X.columns))
        x[0] = sqft
        x[1] = bath
        x[2] = bhk
        if loc_index >= 0:
            x[loc_index] = 1

        return model.predict([x])[0]

    predict_price('1st Phase JP Nagar', 1000, 2, 3)
    ```

## Model Deployment

The trained model and the feature columns are saved as:
- `banglore_home_price_prediction_model.pickle`
- `columns.json`

These files can be used for deploying the model in a web application.
