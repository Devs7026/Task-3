

#  Linear Regression

## Overview

This project predicts housing prices using linear regression on the `Housing.csv` dataset. The workflow includes data cleaning, feature engineering, model training, evaluation, and visualization. The goal is to build an interpretable model and understand the relationships between house features and price.

---


## Steps Performed

### 1. **Data Loading and Inspection**
- Loaded the data using **pandas**.
- Inspected the data for missing values, data types, and summary statistics.

### 2. **Data Cleaning and Preprocessing**
- **Handled missing values** by imputing numerical columns with the median and categorical columns with the mode.
- **Removed outliers** using the IQR (Interquartile Range) method for key numerical features.
- **Encoded categorical variables**:
  - Converted `yes`/`no` columns to 1/0.
  - Used one-hot encoding for `furnishingstatus` (with `drop_first=True` to avoid multicollinearity).
- **Standardized numerical features** using `StandardScaler` to improve model performance.

### 3. **Feature Engineering**
- Created new features (e.g., `price_per_sqft`) to enhance predictive power.

### 4. **Model Building**
- Split the data into training and testing sets (70/30 split).
- Trained a **Linear Regression** model using **scikit-learn**.

### 5. **Model Evaluation**
- Evaluated the model using:
  - **Mean Absolute Error (MAE)**
  - **Mean Squared Error (MSE)**
  - **R-squared (R²) Score**
- Interpreted the regression coefficients to understand feature impacts.

### 6. **Visualization**
- Plotted the regression line (predicted vs. actual prices) for area using **matplotlib**.
- Visualized model fit and residuals.

---

## Results

- **MAE:** ~800,109
- **MSE:** ~1,127,740,274,450
- **R²:** ~0.647

These results indicate that the model explains about 65% of the variance in housing prices, with an average prediction error of around ₹8 lakh.

---

## Key Libraries Used

- **pandas** — Data manipulation and analysis
- **numpy** — Numerical computations
- **matplotlib** — Data visualization
- **scikit-learn** — Machine learning, preprocessing, and evaluation
