# COVID-19 Weekly Hospital Admissions Forecasting Using Time Series Models

## Overview

This project aims to forecast weekly COVID-19 confirmed hospital admissions using various time series modeling techniques. The project is organized into two main phases across two Jupyter notebooks:

1. **Data Preparation and Exploration** (Notebook 1)
2. **Modeling and Forecasting** (Notebook 2)

The end goal is to identify the most effective model for forecasting weekly hospital admissions to aid healthcare planning and pandemic preparedness.

---

## Problem Statement

During the COVID-19 pandemic, accurately forecasting hospital admissions has been critical for public health management. Given historical data on confirmed COVID-19 hospital admissions, the objective is to:

- Explore time-dependent patterns
- Develop forecasting models to predict future admissions
- Compare model performance using robust evaluation metrics

---

## Notebooks Breakdown

### 1. capstone_project_group_10.ipynb (Notebook 1)

This notebook focuses on data understanding and preprocessing.

**Key Activities:**
- Imported raw admissions dataset (`RVR.csv`)
- Explored column types and performed data cleaning
  - Removed duplicates
  - Handled missing values
- Parsed and formatted `collection_date` as a datetime object
- Plotted raw hospital admissions to inspect trends
- Applied **seasonal decomposition** using `statsmodels` to detect:
  - Long-term trends
  - Seasonal effects
  - Irregular components

The goal here was to understand the structure of the time series and prepare it for modeling in the next phase.

---

### 2. LSTM_Prediction_Model.ipynb (Notebook 2)

This notebook contains the modeling workflow using five different forecasting techniques.

**Data Preparation:**
- Created lag features (`lag_1` to `lag_5`) to capture temporal dependencies
- Split data into training and testing sets (80/20 split)
- Filled missing values in lag features with zeros

**Models Implemented:**

1. **Linear Regression**
   - Simple baseline model using lagged features
   - Fast to train and interpret

2. **SARIMAX (Seasonal ARIMA with eXogenous variables)**
   - Captures autoregressive (AR), integrated (I), and moving average (MA) components
   - Handles seasonality effectively
   - Parameter tuning performed using grid search

3. **Facebook Prophet**
   - Robust time series library developed by Meta
   - Decomposes data into trend, seasonality, and holiday effects
   - Automatically detects changepoints and seasonality

4. **LSTM (Long Short-Term Memory)**
   - Deep learning model using Keras
   - Suitable for capturing long-term dependencies in time series
   - Data reshaped into 3D tensors for sequential learning

5. **Vector AutoRegression (VAR)**
   - Multivariate time series model
   - Leverages lag relationships between multiple time-dependent variables

**Evaluation Metrics:**
- **Mean Absolute Error (MAE)**
- **Mean Squared Error (MSE)**
- **R-squared (R²)**
- **Visual comparison**: Actual vs Predicted plots

Each model’s forecast was plotted against the actual values to assess temporal accuracy and overfitting risks.

---

## Dataset Details

- **Filename**: `RVR.csv`
- **Source**: Presumed weekly COVID-19 hospital admissions records
- **Target Variable**: `average_admissions_all_covid_confirmed`
- **Time Index**: `collection_date`

**Note:** Lagged features (`lag_1` to `lag_5`) are engineered in Notebook 2.

---

## Installation & Setup

Ensure the following packages are installed:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow statsmodels prophet sktime
