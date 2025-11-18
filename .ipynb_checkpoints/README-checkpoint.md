# Wildfire Data Analysis Project

This repository contains our analysis of U.S. wildfires (1992–2020) with a primary focus on Georgia. We aim to (a) classify wildfire **cause** and **severity/size category**, and (b) model **burned area** with regression, using both wildfire records and daily climate variables.

## Data sources
- **Wildfire records:** US wildfire database (1992–2020), with location, date, cause, and size.
- **Climate:** Daily max temperature, max wind, and min relative humidity from GA weather stations, consolidated to align with wildfire locations/dates.

## Tasks & models
- **Classification:** Multinomial Logistic Regression; Tree-based models (Random Forest, Gradient Boosting) for nonlinearity & feature importance.
- **Regression:** Regularized linear models (Ridge, LASSO, Elastic Net) to predict burned area and handle collinearity.
- **Evaluation:**
  - Classification: Accuracy, Precision, Recall, F1.
  - Regression: RMSE, MAE, R².

## Cross-validation strategy (spatiotemporal blocking)
- **Temporal split:** Train on earlier years (e.g., 1992–2015), test on later years (e.g., 2016–2020).
- **Spatial blocking:** Partition Georgia into regions (e.g., north vs. south) to reduce spatial leakage during validation.