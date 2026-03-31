# Room_7_Bakery_Prediction - Bakery Sales Forecasting

## Repository Link

[https://github.com/lasse-fr/Room_7_Bakery_Prediction](https://github.com/lasse-fr/Room_7_Bakery_Prediction)

## Description

This project focuses on sales forecasting for a bakery branch, utilizing historical sales data spanning from July 1, 2013, to July 30, 2018, to inform inventory and staffing decisions. We aim to predict future sales for six specific product categories: Bread, Rolls, Croissants, Confectionery, Cakes, and Seasonal Bread. Our methodology integrates data preparation, exploratory data analysis, baseline linear regression modeling, and advanced machine learning techniques including Ridge, Lasso, ElasticNet, and Random Forest regression. The project evaluates model performance on test data from August 1, 2018, to July 30, 2019, using the Mean Absolute Percentage Error (MAPE) and R² metrics.

## Task Type

**Regression** - Predicting continuous numerical values (sales amounts in EUR) for six product categories.

## Results Summary

### Best Model Performance

| Model | Training MAPE | Validation MAPE | Training R² | Validation R² |
|-------|---------------|-----------------|-------------|---------------|
| Baseline (Linear Regression) | 28.87% | 32.76% | 0.7718 | 0.7139 |
| Ridge Regression | 28.24% | 31.96% | 0.7856 | 0.7272 |
| Lasso Regression | 28.19% | 31.96% | 0.7798 | 0.7189 |
| **ElasticNet** | **28.16%** | **31.93%** | **0.7863** | **0.7278** |
| **Random Forest** | **13.42%** | **20.39%** | **0.9033** | **0.8497** |

**Best Performing Model: Random Forest** with a validation MAPE of **20.39%** and R² of **0.8497**.

### Model Comparison

| Model | Key Characteristics | Validation MAPE | Validation R² |
|-------|---------------------|-----------------|---------------|
| Linear Regression | Simple baseline with 50 raw features | 32.76% | 0.7139 |
| Ridge Regression | L2 regularization, handles multicollinearity | 31.96% | 0.7272 |
| Lasso Regression | L1 regularization, feature selection | 31.96% | 0.7189 |
| ElasticNet | Combined L1+L2 regularization (best linear) | 31.93% | 0.7278 |
| **Random Forest** | Ensemble of 100 trees, 117 features, max depth 20 | **20.39%** | **0.8497** |

### Result by Category (Random Forest - Validation MAPE)

- **Bread (1):** 40.03%
- **Rolls (2):** 26.44%
- **Croissant (3):** 19.87%
- **Confectionery (4):** 48.49%
- **Cake (5):** 16.71%
- **Seasonal Bread (6):** 64.77%

## Key Insights

1. **Product Category Dominance:** Warengruppe (product category) is by far the most important feature, contributing over 71% to the Random Forest's predictive power.
2. **Seasonality Matters:** Season and day-of-week are the second and third most important features, reflecting strong weekly and seasonal sales patterns.
3. **Weather Impact:** Temperature and wind speed have measurable effects on bakery sales, with warmer days generally correlating with higher sales.
4. **Kieler Woche Effect:** The annual Kiel Week festival significantly boosts sales across all product categories.
5. **Advanced Models Outperform:** Random Forest reduced the validation MAPE from 31.93% (best linear model) to 20.39%, a ~36% relative improvement.
6. **Feature Engineering Success:** Engineering 60+ features including lag variables, moving averages, holiday flags, and weather categories improved model performance substantially.
7. **Category-Specific Challenges:** Seasonal Bread (G6) remains the hardest to predict (MAPE 64.77%), while Cake (G5) is the most predictable (MAPE 16.71%).

## Team Members

| # | Name | GitHub |
|---|------|--------|
| 1 | Lasse Frohnert | [@lasse-fr](https://github.com/lasse-fr) |
| 2 | Farida Rahimova | [@Betria0](https://github.com/Betria0) |
| 3 | Vikram Vupparapalli | [@vupparapallivikram](https://github.com/vupparapallivikram) |

## Contribution Split

| Team Member | Main Contributions |
|-------------|-------------------|
| Lasse Frohnert | Data preparation notebooks, Advanced LR models (Ridge/Lasso/ElasticNet), Random Forest implementation, feature engineering |
| Farida Rahimova | Dataset characteristics analysis, correlation studies, missing data analysis |
| Vikram Vupparapalli | Data analysis (Umsatz, Kiwo, Wetter), model evaluation, predictions generation | Baseline model development, data merging (Umsatz/Kiwo/Wetter), feature engineering

## Documentation

1. [**Data Import and Preparation**](https://github.com/lasse-fr/Room_7_Bakery_Prediction/blob/main/0_DataPreparation) - Merging Umsatz, Kiwo, and Wetter datasets; adding holidays and vacation flags; engineering 60+ features including lags, moving averages, and interaction terms.
2. [**Dataset Characteristics (Barcharts)**](https://github.com/lasse-fr/Room_7_Bakery_Prediction/blob/main/1_DatasetCharacteristics) - Exploratory data analysis, missing value analysis, correlation studies, and data visualization.
3. [**Baseline Model**](https://github.com/lasse-fr/Room_7_Bakery_Prediction/blob/main/2_BaselineModel) - Linear regression baseline with 50 features, achieving MAPE 32.76% on validation data.
4. [**Model Definition and Evaluation**](https://github.com/lasse-fr/Room_7_Bakery_Prediction/blob/main/3_Model) - Advanced models including Ridge, Lasso, ElasticNet, and Random Forest with comprehensive evaluation metrics and feature importance analysis.
5. [**Presentation**](https://github.com/lasse-fr/Room_7_Bakery_Prediction/blob/main/4_Presentation/README.md) - Project slides and final presentation materials.

## Cover Image

![Cover Image](https://github.com/lasse-fr/Room_7_Bakery_Prediction/blob/main/CoverImage/cover_image.png)
