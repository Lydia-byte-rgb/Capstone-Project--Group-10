# Forecasting and Monitoring Hospitalization Trends from Respiratory Viruses in Kenya  
(Using U.S. Government Data as a Proxy)

## Project Overview

Kenya faces challenges in tracking and predicting hospitalizations caused by respiratory viruses like COVID-19, Influenza, and RSV due to limited real-time health data. This project leverages publicly available hospitalization data from the United States (from CDC and HHS) as a proxy dataset.

Using this structured data, we build a pipeline to:
- Analyze hospitalization trends
- Engineer time series features
- Train forecasting models
- Evaluate prediction accuracy

These insights are designed to guide the development of similar systems in Kenya when comparable data becomes available.

---

## Project Structure

- `capstone_project_group_10.ipynb`: Exploratory Data Analysis (EDA) and preprocessing
- `Final_Model_Notebook.ipynb`: Model training, evaluation, and forecasting
- `/images`: Contains all output visualizations used below

---

## Exploratory Data Analysis (EDA)

Initial exploration includes:
- Temporal trends by virus
- Hospital admissions by state and region
- Missing data heatmaps
- Weekly patterns

---

## Data Preparation & Feature Engineering

To prepare the data for time series modeling:
- Lag features and rolling statistics were added
- Weekly grouping was applied
- Target variable was renamed for modeling compatibility
- SMA (Simple Moving Average) was also computed for benchmarking

---

## Machine Learning Models

We used Random Forest Regressor as the primary model. Additional techniques include:
- GridSearchCV for hyperparameter tuning
- Cross-validation
- Feature importance analysis

---

### Model Performance Visualizations

#### Random Forest Predictions vs Actuals
![RF vs Actual](images/model_plot_1.png)

#### Feature Importance from Random Forest
![Feature Importance](images/model_plot_2.png)

#### Residual Plot
![Residuals](images/model_plot_3.png)

#### Forecast vs Actual (Full Test Set)
![Full Forecast](images/model_plot_4.png)

#### SMA Baseline Comparison
![SMA Baseline](images/model_plot_5.png)

#### County-Specific Forecasts (Examples)

Example 1  
![County Forecast 1](images/model_plot_6.png)

Example 2  
![County Forecast 2](images/model_plot_7.png)

Example 3  
![County Forecast 3](images/model_plot_8.png)

#### Additional Evaluation Visuals

Prediction error histogram  
![Error Histogram](images/model_plot_9.png)

Forecast windows comparison  
![Forecast Windows](images/model_plot_10.png)

---

## Conclusion

This project demonstrates a scalable pipeline for forecasting respiratory-related hospitalizations. By using U.S. data as a stand-in, we can design robust forecasting systems that will be critical when similar healthcare infrastructure is developed in Kenya.

---

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name

