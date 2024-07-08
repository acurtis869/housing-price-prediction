# Housing Price Prediction Model

## Overview

This project involves developing a predictive model for housing prices using a sample from a large dataset. The model is created using Python libraries and various machine learning techniques to handle data preprocessing, model training, and evaluation.

## Steps

### 1. Data Preparation
- **Import Libraries:** Utilises `numpy`, `pandas`, and `matplotlib` for data manipulation and visualisation.
- **Load Dataset:** Reads a large housing dataset, then randomly samples 100,000 rows for analysis.
- **Data Filtering:** Filters columns of interest: property type, estate type, and location. Transforms the location column into a binary variable indicating whether the property is in London.
- **Handle Missing Values:** Ensures there are no missing values in the dataset.
- **One-Hot Encoding:** Applies one-hot encoding to categorical variables using Scikit-Learn's `OneHotEncoder`.
- **Data Splitting:** Splits data into training and testing sets based on the date, using pre-2017 data for training and the rest for testing.

### 2. Exploratory Data Analysis
- **Label Distribution:** Examines the distribution of house prices, noting a heavy right-skew.
- **Log Transformation:** Applies a log transformation to the house prices to achieve a more normal distribution.

### 3. Model Exploration
- **Linear Regression:** Implements a basic linear regression model and evaluates it using 10-fold cross-validation.
- **Decision Tree Regressor:** Evaluates a decision tree model using the same cross-validation technique.
- **Random Forest Regressor:** Uses a random forest model, which performs slightly better than the decision tree model.

### 4. Model Fine-Tuning
- **Grid Search:** Conducts a grid search to fine-tune the hyperparameters of the random forest model.
- **Hyperparameter Optimisation:** Identifies the best hyperparameters and performs a second grid search to further refine the model.

### 5. Model Evaluation and Presentation
- **Model Evaluation:** Uses the test data to evaluate the final model, calculating the root mean squared error (RMSE).
- **Feature Importance:** Analyses the importance of each feature in the final model, with the binary 'London' variable being the most significant predictor.

## Conclusion

The final model demonstrates good predictive power with an RMSE that is less than 8% of the mean log house price. The 'London' variable is identified as the most critical feature in predicting housing prices.