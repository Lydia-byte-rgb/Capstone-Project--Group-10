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

We used Linear regression as our baseline model. Other models we used were random forest and XGBoost as shown below.

---

### Model Performance Visualizations
### Plot predictions vs actual for Linear Regression
![image](https://github.com/user-attachments/assets/4dc3c436-6271-4943-b3df-fa9c619a3892)

#### Random Forest Predictions vs Actuals
![image](https://github.com/user-attachments/assets/f749d9fc-72a7-404c-8121-4850a95f6624)

#### XGBOOST MODEL Actual vs Predicted results
![image](https://github.com/user-attachments/assets/546fad9f-ab55-443b-ab74-46c76987fd99)

#### Comparison of baseline models (Linear Regression, Random Forest, XGBoost)
![image](https://github.com/user-attachments/assets/4061663f-3c87-4826-93b6-a3097b55ad68)


### Deep Learning Models
LSTM model Actual vs Predicted Hospital admissions
![image](https://github.com/user-attachments/assets/267aab50-1462-4842-9ee8-0526aca0ec93)


### Time Series Models
NAIVE FORECAST MODEL
![image](https://github.com/user-attachments/assets/479a9341-493c-4104-840e-28de5a8dbbb0)
This is was our baseline time series model

#### PROPHET MODEL
Actual vs Predicted admissions
![image](https://github.com/user-attachments/assets/21d638af-602c-42b7-8319-bc68becf76cb)

#### VAR MODEL actual vs predicted admissions
![image](https://github.com/user-attachments/assets/0c307da3-8383-475e-aa99-d8a3bba40b17)


#### SARIMA MODEL Actual vs Predicted admissions
![image](https://github.com/user-attachments/assets/f292a831-7f45-4b16-8996-d791d2194d29)

### Time Series Model Comparison
![image](https://github.com/user-attachments/assets/f0e636f9-8726-499f-b858-e6229490b9e8)

Comparison of Random Forest, LSTM, and SARIMA
![image](https://github.com/user-attachments/assets/03970e71-d762-40f2-9772-0f3598f743a2)

### Deployment images
We locally deployed the SARIMA model using streamlit on ngrok app and the images below show the output.
![image](https://github.com/user-attachments/assets/f8736de7-fe6a-46c1-a2c6-895aad653af0)
![image](https://github.com/user-attachments/assets/a9e47f75-b60b-402e-81f9-eeaaa1b4a77a)

---

## Conclusion

This project demonstrates a scalable pipeline for forecasting respiratory-related hospitalizations. By using U.S. data as a stand-in, we can design robust forecasting systems that will be critical when similar healthcare infrastructure is developed in Kenya.

---

## Tableau link
[tableau](https://public.tableau.com/views/Book2_17413502549780/HospitalizationTrendsacrossthecountry?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
