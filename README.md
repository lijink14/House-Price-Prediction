# House Price Prediction using Ridge and Lasso Regression

## Project Overview

This project aims to predict house prices using a dataset from a US-based housing company entering the Australian market. The models built in this project help identify significant predictors and provide robust, generalizable predictions for house prices.

## Objectives

1. **Identify Significant Variables:** Determine which features significantly influence house prices.
2. **Build Predictive Models:** Use Ridge and Lasso regression techniques to build and evaluate predictive models.
3. **Optimize Alpha Values:** Find the optimal values for the regularization parameter (alpha) in Ridge and Lasso regression.
4. **Handle Missing Data:** Re-train models excluding the most important features when they are unavailable.
5. **Ensure Robustness:** Ensure the models are robust and generalizable to new data.

## Dataset

The dataset used in this project contains various features related to houses, such as `OverallQual`, `GrLivArea`, `GarageCars`, `TotalBsmtSF`, `YearBuilt`, and many others. The dataset is divided into training and testing sets to evaluate model performance.

## Methodology

### Data Preprocessing

- **Handling Missing Values:** Missing values were filled using appropriate strategies like median, zeroes, or the most frequent value.
- **Encoding Categorical Variables:** Categorical variables were converted to numerical values using OneHotEncoder.
- **Scaling:** Numerical features were scaled using StandardScaler.
- **Dimensionality Reduction:** PCA was applied to reduce the number of features while preserving 95% of the variance.

### Model Building

1. **Ridge Regression:**
   - Applied Ridge regression with GridSearchCV to find the optimal alpha.
   - Evaluated model performance using RMSE and R² scores.

2. **Lasso Regression:**
   - Applied Lasso regression with GridSearchCV to find the optimal alpha.
   - Evaluated model performance using RMSE and R² scores.

### Results

- **Ridge Regression:**
  - Optimal alpha: 100.0
  - RMSE: 35,665.15
  - R²: 0.834

- **Lasso Regression:**
  - Optimal alpha: 100.0
  - RMSE: 35,145.09
  - R²: 0.839

### Re-training Without Top Predictors

- Identified the top 5 predictors using the initial Lasso model.
- Re-trained the models after removing these top predictors to identify the next set of important features.

### Ensuring Robustness

- Used cross-validation to ensure the models generalize well to new data.
- Applied regularization techniques to prevent overfitting.
- Conducted hyperparameter tuning for optimal performance.

## How to Run

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/house-price-prediction.git
   cd house-price-prediction
