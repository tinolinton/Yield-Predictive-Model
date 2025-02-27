# Yield-Predictive-Model

This project aims to predict agricultural yield using various machine learning models, including XGBoost, Linear Regression, Random Forest, and Artificial Neural Networks (ANN). The dataset used for this project is the Agricultural Survey Dataset.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Preprocessing](#preprocessing)
- [Model Training and Tuning](#model-training-and-tuning)
- [Model Evaluation](#model-evaluation)
- [Feature Importance](#feature-importance)
- [Hyperparameter Tuning](#hyperparameter-tuning)
- [Visualization](#visualization)
- [Setup and Installation](#setup-and-installation)
- [Conclusion](#conclusion)

## Introduction

The goal of this project is to build predictive models to estimate agricultural yield based on various features such as area under crop, value of pesticides/herbicides used, fertilizer used, average rainfall, and average temperature.

## Dataset

The dataset used in this project is the Agricultural Survey Dataset, which contains the following columns:

- `year`: Year of the survey
- `district`: District where the survey was conducted
- `farm_id`: Unique identifier for each farm
- `area_under_crop`: Area under crop in hectares
- `sector`: Sector of the farm
- `crop_type`: Type of crop grown
- `value_pesticides/herbicides`: Value of pesticides/herbicides used
- `fertilizer_used_kg/hectare`: Fertilizer used in kg per hectare
- `average_rainfall`: Average rainfall in mm
- `average_temperature`: Average temperature in degrees Celsius
- `yield`: Yield in tonnes

## Exploratory Data Analysis (EDA)

EDA was performed to understand the distribution and relationships of the features in the dataset. Key steps included:

- Displaying the first few rows of the dataset
- Checking for missing values
- Descriptive statistics of selected columns
- Visualizing the number of records per district and sector
- Calculating and plotting the average yield per hectare by crop type and year
- Visualizing the distribution of numerical features and count plots of categorical features
- Boxplots for numerical features

![EDA Visualization](images/eda_visualization.png)

## Preprocessing

Preprocessing steps included:

- Dropping the `farm_id` column
- Handling missing values by filling them with the median for numerical columns
- Detecting and handling outliers using the Interquartile Range (IQR) method
- Normalizing numerical features using MinMaxScaler
- Encoding categorical features using one-hot encoding

## Model Training and Tuning

Four machine learning models were trained and tuned:

1. **Linear Regression**
2. **Random Forest Regressor**
3. **XGBoost Regressor**
4. **Artificial Neural Network (ANN)**

Each model was trained on the preprocessed dataset, and predictions were made on the test set.

## Model Evaluation

The models were evaluated using the following metrics:

- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- R² Score

The evaluation results were compared across models to determine the best-performing model.

![Model Evaluation](images/model_evaluation.png)

## Feature Importance

Feature importance was calculated for each model to understand the contribution of each feature to the predictions. The importance scores were aggregated and visualized.

![Feature Importance](images/feature_importance.png)

## Hyperparameter Tuning

Hyperparameter tuning was performed for the XGBoost and Random Forest models using GridSearchCV. The best parameters were identified, and the models were retrained with these optimal parameters.

## Visualization

Various visualizations were created to understand the data and model performance, including:

- Bar plots for the number of records per district and sector
- Bar plots for average yield per hectare by crop type and year
- Distribution plots for numerical features
- Count plots for categorical features
- Boxplots for numerical features
- Comparison plots for model predictions vs. true values
- Bar plots for aggregated feature importance

![Visualization](images/visualization.png)

## Setup and Installation

To set up and run this project, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/Yield-Predictive-Model.git
    cd Yield-Predictive-Model
    ```

2. Create and activate a virtual environment:
    ```sh
    python -m venv venv
    venv\Scripts\activate  # On Windows
    source venv/bin/activate  # On macOS/Linux
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

4. Run the Jupyter Notebook:
    ```sh
    jupyter notebook models.ipynb
    ```

## Conclusion

This project demonstrates the process of building and evaluating predictive models for agricultural yield using various machine learning techniques. The results show that different models have varying levels of performance, and hyperparameter tuning can significantly improve model accuracy.
