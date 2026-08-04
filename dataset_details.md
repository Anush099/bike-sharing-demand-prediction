# Dataset Details

## Project Title

**Predicting Urban Bike Sharing Demand Using Weather, Seasonal, and Calendar-Based Machine Learning Features**

## Overview

This project uses two publicly available bike-sharing datasets. The **Seoul Bike Sharing Demand dataset** is used as the primary dataset for the main machine learning implementation. The **Washington D.C. Bike Sharing dataset** is used as a parallel dataset to test whether the same modelling workflow performs effectively on another city’s bike-sharing data.

---

## 1. Primary Dataset: Seoul Bike Sharing Demand Dataset

### Dataset Source

**UCI Machine Learning Repository**

### Dataset Link

https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand

### Description

The Seoul Bike Sharing Demand dataset contains hourly bike rental records from the Seoul bike-sharing system. It includes weather, seasonal, holiday and operational information that can be used to predict hourly bike rental demand.

### Target Variable

`Rented Bike Count`

### Main Features

- Date
- Hour
- Temperature
- Humidity
- Wind speed
- Visibility
- Dew point temperature
- Solar radiation
- Rainfall
- Snowfall
- Seasons
- Holiday
- Functioning Day

### Use in This Project

This dataset was used as the main dataset for:

- Data preprocessing
- Exploratory Data Analysis
- Feature engineering
- Model training
- Model evaluation
- K-Fold cross-validation
- Time-series cross-validation
- Feature-importance analysis
- Functioning-day ablation testing

### Models Applied

- Linear Regression
- Random Forest
- Gradient Boosting
- XGBoost

### Best Result on Seoul Dataset

| Best Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| XGBoost | 94.535 | 161.006 | 0.938 |

---

## 2. Parallel Dataset: Washington D.C. Bike Sharing Dataset

### Dataset Source

**UCI Machine Learning Repository**

### Dataset Link

https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset

### Description

The Washington D.C. Bike Sharing dataset contains hourly bike rental records from the Capital Bikeshare system. It includes time, calendar and weather-related variables suitable for bike-sharing demand prediction.

### Original Target Variable

`cnt`

### Renamed Target Variable in This Project

`Rented_Bike_Count`

### Main Features

- Date
- Season
- Year
- Month
- Hour
- Holiday
- Weekday
- Working day
- Weather situation
- Temperature
- Feeling temperature
- Humidity
- Wind speed

### Important Preprocessing Note

The columns `casual` and `registered` were removed before modelling because they directly contribute to the target variable `cnt`.

Keeping these columns would cause **target leakage** and produce unrealistic model performance.

### Use in This Project

This dataset was used as a parallel dataset to:

- Test the developed workflow on another city’s bike-sharing data
- Compare model performance across two datasets
- Perform additional cross-validation
- Strengthen the reliability of the findings
- Show that the modelling approach is not limited to one dataset only

### Models Applied

- Linear Regression
- Random Forest
- Gradient Boosting
- XGBoost

### Best Result on Washington D.C. Dataset

| Best Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| XGBoost | 25.717 | 40.549 | 0.948 |

---

## 3. Purpose of Using Two Datasets

The Seoul dataset was used as the primary dataset for model development and evaluation. The Washington D.C. dataset was added as a parallel dataset based on supervisor feedback.

Using both datasets helped to:

- Compare model performance across different urban bike-sharing systems
- Check whether the modelling workflow generalises beyond one dataset
- Evaluate model reliability using a second dataset
- Support the final discussion and results chapter with comparative evidence

---

## 4. Final Note

Both datasets are publicly available and were used only for academic research purposes. The project does not use personal, private or sensitive user information.
