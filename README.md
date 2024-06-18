# Housing Price Prediction Project

This project aims to predict housing prices using various regression models. The dataset used is from a housing dataset containing information about different houses' geographical location, median age, number of rooms, population, and other features.

## Dataset

The dataset contains the following columns:

- `longitude`
- `latitude`
- `housing_median_age`
- `total_rooms`
- `total_bedrooms`
- `population`
- `households`
- `median_income`
- `median_house_value`
- `ocean_proximity`

## Data Preprocessing

1. **Handling Missing Values**:
   - Dropped rows with missing values in the `total_bedrooms` column.

2. **Log Transformation**:
   - Applied log transformation to `total_rooms`, `total_bedrooms`, `population`, and `households` to reduce skewness.

3. **One-Hot Encoding**:
   - Converted categorical `ocean_proximity` column to dummy variables.

4. **Feature Scaling**:
   - Scaled the features using `StandardScaler`.

## Exploratory Data Analysis (EDA)

- Plotted histograms for numerical columns before and after log transformation.
- Created a heatmap to visualize the correlation between features.
- Used scatter plots to understand geographical distribution.

## Model Training and Evaluation

### Models Used

1. **Linear Regression**
2. **Ridge Regression**
3. **Lasso Regression**
4. **Random Forest Regressor**
5. **Gradient Boosting Regressor**
6. **XGBoost Regressor**
7. **Decision Tree Regressor**

### Model Evaluation

The models were evaluated using Root Mean Squared Error (RMSE) and R² score.

| Model                  | RMSE           | R² Score        |
|------------------------|----------------|-----------------|
| Linear Regression      | 67775.13       | 0.664           |
| Ridge Regression       | 67742.03       | 0.664           |
| Lasso Regression       | 67699.92       | 0.665           |
| Random Forest          | 48516.43       | 0.828           |
| Gradient Boosting      | 56816.72       | 0.764           |
| XGBoost                | 49541.45       | 0.821           |
| Decision Tree          | 67766.99       | 0.664           |

Random Forest Regressor performed the best with the lowest RMSE and highest R² score.


