---
# House Price Prediction Project

This project involves predicting house prices using machine learning models. The dataset used for this analysis is the **`kc_house_data.csv`** file. The goal is to select relevant features based on their correlation with the target variable (`price`) and build predictive models using Ridge Regression and XGBoost.

---

## Table of Contents

1. [Introduction](#introduction)  
2. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)  
3. [Feature Selection](#feature-selection)  
4. [Model Building](#model-building)   
5. [Conclusion](#conclusion)  

---

## Introduction

Predicting house prices is a common problem in the real estate industry. By analyzing historical data, we can uncover relationships between features and prices, allowing us to make informed predictions for new data.  
This project uses **Ridge Regression** and **XGBoost** for building predictive models and evaluates their performance using metrics like **R² Score** and **Mean Absolute Percentage Error (MAPE)**.

---

## Exploratory Data Analysis (EDA)

1. **Dataset Overview**:
   - Shape of the dataset: `(rows, columns)`  
   - Basic info: Column types and missing values visualized with the `missingno` library.

2. **Correlation Matrix**:  
   - Visualized using a heatmap to identify relationships between features.  
   - Features strongly correlated with the target variable (`price`) were selected for model building.

3. **Pairwise Relationships**:
   - **Price vs. Square Footage**: Strong positive correlation.  
   - **Price vs. Bathrooms**: Weak positive correlation.  

---

## Feature Selection

1. **Threshold Selection**:
   - Features with an absolute correlation greater than **0.3** with the target variable (`price`) were selected.  
   - New dataset created with only the selected features.

2. **Missing Values**:
   - Verified and summarized for the selected features.  

---

## Model Building

### Preprocessing  
- **Train-Test Split**:  
  - Split dataset into training (80%) and testing (20%) subsets.  
- **Feature Scaling**:  
  - Applied `StandardScaler` to normalize the data.  

### Ridge Regression  
- **Hyperparameters**:  
  - Alpha = 10  
- **Performance Metrics**:  
  - R² Score  
  - Mean Absolute Percentage Error (MAPE)  
- **Cross-Validation**:  
  - 10-fold cross-validation applied to both training and testing sets.  

### XGBoost Regressor  
- **Hyperparameters**:  
  - Number of Estimators: 200  
  - Learning Rate: 0.01  
  - Maximum Depth: 5  
  - Alpha: 0.1  
  - Lambda: 1 (Regularization)  
- **Performance Metrics**:  
  - R² Score  
  - Mean Absolute Percentage Error (MAPE)  
- **Cross-Validation**:  
  - 10-fold cross-validation applied to both training and testing sets.  

---

## Conclusion

1. **Model Insights**:  
   - XGBoost outperforms Ridge Regression in predictive performance, especially on the testing set.  
2. **Feature Importance**:  
   - Larger square footage is the most significant predictor of house prices.  
3. **Future Work**:  
   - Experiment with other algorithms and feature engineering techniques to further improve model performance.  

---
