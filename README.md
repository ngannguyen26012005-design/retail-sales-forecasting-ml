# retail-sales-forecasting-ml
A machine learning pipeline for retail sales forecasting using Decision Trees and extensive feature engineering (lags, rolling statistics), achieving an R² score of 0.6083.
# Predictive Analytics in Retail Supply Chain Management: Machine Learning Approaches for Demand Forecasting

## 1. Executive Summary

This project develops a machine learning framework for retail demand forecasting using transactional sales data. The objective is to improve inventory planning and supply chain decision-making by predicting future unit sales through data preprocessing, feature engineering, and machine learning regression models.

The study compares Support Vector Regression (SVR) and Decision Tree Regression models using engineered temporal features and evaluates forecasting performance through RMSE, MAE, and R² metrics.


## 2. Dataset Overview

**Dataset:** Corporación Favorita Grocery Sales Dataset

### Variables Used

#### Target Variable
- `unit_sales`

#### Predictor Variables
- `onpromotion`
- `store_type`
- `cluster`
- `state`
- `date`

### Dataset Characteristics

- Daily retail transaction records
- Multiple stores and product categories
- Promotional campaigns affecting demand
- Strong temporal and seasonal sales patterns


## 3. Key Skills Demonstrated

- Time Series Feature Engineering
- Machine Learning Regression
- Hyperparameter Optimization
- Cross-Validation
- Forecasting Analytics
- Supply Chain Analytics
- Data Preprocessing
- Feature Importance Analysis


## 4. Project Workflow

```text
Raw Retail Data
      ↓
Data Cleaning & Preprocessing
      ↓
Exploratory Data Analysis (EDA)
      ↓
Feature Engineering
      ↓
Encoding & Transformation
      ↓
Model Training
      ↓
Grid Search Cross-Validation
      ↓
Model Evaluation
      ↓
Feature Importance Analysis
```

## 5. Data Preprocessing & Feature Engineering

### Data Preprocessing

To improve model performance and data quality, several preprocessing techniques were applied:

- Logarithmic transformation of `unit_sales` to reduce skewness and stabilize variance.
- Label Encoding for ordinal categorical variables.
- One-Hot Encoding for nominal categorical variables.
- Missing value inspection and consistency checks.

### Feature Engineering

Several predictive variables were constructed to capture demand dynamics.

#### Lag Feature

**sales_lag_1**
- Previous-day sales volume
- Captures short-term demand persistence

#### Rolling Statistics

**rolling_mean_3**
- 3-day moving average
- Captures short-term demand trends

**rolling_mean_7**
- 7-day moving average
- Captures weekly demand behavior

#### Promotion Feature

**onpromotion**
- Captures promotional effects on retail demand

## 6. Predictive Modeling Framework

### Model 1: Support Vector Regression (SVR)

Hyperparameters optimized:
- `C`
- `epsilon`

Purpose:
- Capture potentially non-linear relationships between explanatory variables and sales volume.

### Model 2: Decision Tree Regression

Hyperparameters optimized:
- `max_depth`
- `min_samples_split`

Purpose:
- Learn hierarchical decision rules and provide interpretable predictions.

### Hyperparameter Optimization

Grid Search Cross-Validation was used to identify the best model configuration and improve out-of-sample generalization.

## 7. Model Evaluation Results

The forecasting models were evaluated using standard regression metrics:

| Model | RMSE | MAE | R² |
|--------|--------|--------|--------|
| Support Vector Regression (SVR) | 0.8123 | 0.6145 | 0.1245 |
| Decision Tree Regression (Optimized) | **0.5412** | **0.3854** | **0.6083** |

### Key Findings

- The optimized Decision Tree model achieved the strongest predictive performance.
- The model explained approximately **60.83%** of out-of-sample variation in retail demand.
- Decision Tree Regression substantially outperformed SVR on this dataset.

## 8. Feature Importance Analysis

Feature importance analysis identified the most influential predictors:

1. `rolling_mean_3`
2. `rolling_mean_7`
3. `sales_lag_1`

These results indicate that recent sales history and short-term demand trends are the strongest drivers of future retail sales.


## 9. Business Implications

The optimized Decision Tree model provides both predictive accuracy and interpretability.

Potential applications include:

- Inventory optimization
- Demand forecasting
- Procurement planning
- Safety stock management
- Promotion planning
- Supply chain decision support

Because the model produces transparent decision rules, it can be more easily interpreted and validated by business managers than many black-box alternatives.


## 10. Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- Jupyter Notebook



## 11. Repository Structure

```text
├── Retail_Sales_Forecasting_ML.ipynb
├── Retail_Sales_Forecasting_Report.pdf
├── README.md
└── dataset/
```

### File Description

#### Retail_Sales_Forecasting_ML.ipynb
- Data preprocessing
- Feature engineering
- Model training
- Hyperparameter tuning
- Model evaluation

#### Retail_Sales_Forecasting_Report.pdf
- Full project report
- Methodology discussion
- Experimental results

#### README.md
- Project documentation and overview



## Author

**Nguyen Thai Ngan**  
Bachelor of Economic Mathematics  
University of Economics and Law (UEL)

### Research Interests

- Machine Learning
- Data Science
- Financial Mathematics
- Risk Analytics
- Operational Researc
