# House Prices Prediction

This project is a simple data analysis and machine learning application to predict house prices using the King County housing dataset.

## Project Overview

The dataset contains information about houses, including features such as:

- Bedrooms
- Bathrooms
- Square footage of living space (`sqft_living`)
- Floors
- Waterfront, view, condition, and grade
- Year built and year renovated
- Lot size (`sqft_lot`)

The dataset has **21 columns and 21,613 rows**.

---

## Steps Performed

1. **Data Loading and Inspection**
   - Loaded the dataset using pandas.
   - Checked the shape, data types, missing values, and duplicates.
   - Dropped unnecessary columns (`id`, `zipcode`, `lat`, `long`, `date`).

2. **Exploratory Data Analysis (EDA)**
   - Descriptive statistics to understand the distribution of features.
   - Visualizations:
     - Histograms and box plots for price.
     - Count plots for bedrooms, bathrooms, floors, and grades.
     - Scatter plots to see correlations between features and price.
     - Heatmap to visualize correlations.

3. **Feature Engineering**
   - Created a new feature `age_of_house` = current year - `yr_built`.

4. **Machine Learning**
   - **Single Feature Linear Regression**
     - Predicted house prices using only `sqft_living`.
     - Calculated Mean Squared Error (MSE).
   - **Multivariate Linear Regression**
     - Used multiple features to predict prices.
     - Calculated MSE and model score (R²).

---

## Libraries Used

- `pandas` for data manipulation
- `numpy` for numerical operations
- `matplotlib` and `seaborn` for visualizations
- `plotly` for interactive plots
- `scikit-learn` for machine learning

---

## Results

- Using `sqft_living` alone gave a high MSE (~68 billion), indicating low accuracy.
- Multivariate regression with multiple features improved the prediction (MSE ~47 billion) and achieved an R² score of 0.66.

---

## Conclusion

This project demonstrates basic data analysis and regression modeling for house price prediction. Adding more features or using advanced models could further improve prediction accuracy.
