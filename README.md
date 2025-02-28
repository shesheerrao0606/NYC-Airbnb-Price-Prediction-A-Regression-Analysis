# NYC Airbnb Price Prediction: A Regression Analysis

## Introduction and Data Description

This project analyzes the NYC Airbnb Open Data to understand factors influencing Airbnb listing prices in New York City. Through regression analysis, we aim to identify key price predictors and build models for predicting new listing prices.

### Dataset Description

The dataset contains information about Airbnb listings in NYC, including:

- id: Unique identifier for each listing
- name: Name of the listing
- host_id: Unique identifier for the host
- host_name: Name of the host
- neighbourhood_group: NYC borough (e.g., Manhattan, Brooklyn)
- neighbourhood: Specific neighborhood within the borough
- latitude and longitude: Geographical coordinates of the listing
- room_type: Type of room (e.g., Entire home/apt, Private room)
- price: Price per night
- minimum_nights: Minimum number of nights required to book
- number_of_reviews: Total number of reviews
- last_review: Date of the last review
- reviews_per_month: Average number of reviews per month
- calculated_host_listings_count: Number of listings by the same host
- availability_365: Number of available days within a year
- number_of_reviews_Itm: Number of reviews in the last 12 months
- license: License status
- rating: Rating of the listing
- bedrooms: Number of bedrooms
- beds: Number of beds
- baths: Number of bathrooms

### Importance of Regression Analysis

Regression analysis allows us to examine the relationship between the price of Airbnb listings and various independent variables. This method helps identify significant factors impacting price and quantify their effects, crucial for hosts setting competitive prices and guests seeking value.

## Data Preprocessing

### Exploratory Data Analysis (EDA)

EDA summarizes the main characteristics of the dataset using visual methods to discover patterns, spot anomalies, test hypotheses, and check assumptions.

### Handling Missing Values and Outliers

Steps taken to handle non-numeric values and prepare data:
1. Identify and convert non-numeric values to NaN
2. Impute or drop missing values
3. Ensure numeric data across specified columns
4. Remove rows with NaN values in numerical columns

## Model Selection for Regression Analysis

Several regression models were considered:

1. Linear Regression
2. Polynomial Regression
3. Ridge Regression
4. Lasso Regression
5. Elastic Net Regression
6. Support Vector Regression (SVR)

## Model Evaluation

### Performance Metrics

| Model | Mean Squared Error | Root Mean Squared Error | Mean Absolute Error | Mean Absolute Percentage Error | R^2 Score |
|-------|--------------------|--------------------------|--------------------|--------------------------------|-----------|
| Linear Regression | 90,197.08 | 300.33 | 121.80 | 106.66 | -0.0013 |
| Polynomial Regression (Degree 2) | 89,960.24 | 299.93 | 121.15 | 104.92 | 0.0013 |
| Ridge Regression | 90,196.61 | 300.33 | 121.8 | 106.66 | -0.0013 |
| Lasso Regression | 90,020.80 | 300.03 | 121.37 | 106.21 | 0.0006 |

### Key Observations and Improvements

- All models show significant decrease in MSE compared to previous values
- Polynomial Regression (Degree 2) has the lowest MSE and RMSE
- MAE values have decreased across all models
- MAPE values have improved, with Polynomial Regression showing the lowest percentage error
- R^2 scores have improved but remain close to zero or slightly negative

## Interpretation of Results

### Best Model: Polynomial Regression (Degree 2)

- Quadratic terms represent how the impact of a feature on the target variable changes as the feature's value increases
- Interaction terms represent how the combined effect of two features influences the target variable
- Significant predictors include minimum_nights, number_of_reviews, reviews_per_month, and rating

### Practical Implications

- Insights from feature coefficients can guide pricing strategies and property listing optimizations
- High ratings and frequent reviews could be used as a marketing tool to justify higher prices
<img width="628" alt="image" src="https://github.com/user-attachments/assets/a29185a1-f797-4235-af34-baeec8ee485f" />

## Conclusion

<img width="687" alt="image" src="https://github.com/user-attachments/assets/68c5fad2-edb3-431d-86a3-4aebf699a401" />


### Summary of Key Findings

- Polynomial regression improved model performance metrics significantly
- Models still exhibit low R^2 scores, indicating limited explanatory power

### Limitations

- Feature limitations in capturing complex patterns
- Data quality issues and potential overfitting in polynomial models

### Future Research Directions

- Explore advanced modeling techniques (e.g., ensemble methods, deep learning)
- Further feature engineering and data enrichment
- Fine-tune hyperparameters for Ridge and Lasso regression

These insights can guide efforts in refining predictive models for price forecasting and understanding factors affecting property pricing in the NYC Airbnb market.

<img width="687" alt="image" src="https://github.com/user-attachments/assets/0b1cbfe1-d380-4d93-97b4-27971c55390c" />
