# US Accidents Analysis — End-to-End Data Engineering & Analytics Platform

## Overview

This project builds an end-to-end analytics pipeline for large-scale US traffic accident data, transforming raw records into analytics-ready datasets, predictive models, forecasting outputs, and interactive business intelligence dashboards.

The platform applies **Medallion Architecture (Bronze / Silver / Gold)** to process **500,000 accident records (2016–2023)** and deliver a structured analytics foundation for reporting, machine learning, and forecasting.

---

## Project Objectives

* Build a production-style data engineering pipeline
* Clean and standardize large-scale accident data
* Design a dimensional model for analytics and reporting
* Develop predictive models for accident severity classification
* Forecast future accident trends
* Deliver interactive business dashboards in Power BI

---

## Architecture

Raw CSV Data
→ Bronze Layer (raw ingestion)
→ Silver Layer (cleaning, validation, imputation)
→ Gold Layer (feature engineering + dimensional modeling)
→ Star Schema (fact + dimension tables)
→ Machine Learning
→ Forecasting
→ Power BI Dashboards
→ Microsoft Fabric Lakehouse

---

## Dataset

**US Accidents Dataset (2016–2023)**

* 500,000 records analyzed
* Multi-year traffic accident observations across the United States
* Includes temporal, weather, road infrastructure, geographic, and severity attributes

---

## Pipeline Layers

### Bronze Layer

Raw source ingestion and initial profiling.

**Key tasks**

* Raw dataset loading
* Missing value profiling
* Initial schema inspection

---

### Silver Layer

Data cleaning and quality refinement.

**Key tasks**

* Missing value treatment
* Column standardization
* Feature normalization
* Domain-based imputations
* Zero-row-loss cleaning strategy

---

### Gold Layer

Business-ready analytical layer.

**Key tasks**

* Feature engineering
* Aggregation-ready structures
* Star schema modeling
* Fact and dimension generation

---

## Dimensional Model

### Fact Table

* Accident Fact

### Dimensions

* Date
* Time
* Location
* Weather
* Road Features
* Severity
* Source

This dimensional model supports efficient Power BI analytics and downstream modeling.

---

## Machine Learning

Multiple models were evaluated for accident severity classification.

### Experimental Models

* LightGBM
* XGBoost
* Random Forest
* Logistic Regression
* CatBoost

---

## Production Model

### CatBoost V4 (Production)

* **ROC-AUC:** 74.60%
* **Accuracy:** 69.76%
* **Optimized Threshold:** 0.5034

CatBoost was selected as the production model because it demonstrated the strongest real-world class separation performance.

### Top Features

* Distance (mi)
* Wind Speed
* Year
* Temperature
* Pressure
* Week of Year
* Humidity

---

## Forecasting

A forecasting layer was built using Prophet.

### Forecast Summary

* Historical training period: **87 months**
* Forecast horizon: **12 months**
* Historical accidents: **497K**
* Predicted next 12 months: **124K**
* Peak forecast month: **December**
* Lowest forecast month: **June**

---

## Power BI Dashboards

The project includes **8 interactive dashboards**.

### 1. Executive Overview

* Total accidents
* Average severity
* Average duration
* High severity ratio

### 2. Temporal Analysis

* Yearly trend
* Monthly seasonality
* Day-of-week patterns
* Rush-hour concentration

### 3. Weather & Environment

* Weather type distribution
* Rain, fog, snow analysis
* Visibility impact

### 4. Geography

* State-level accident concentration
* City-level hotspots
* Road corridor analysis

### 5. Road Features

* Junctions
* Signals
* Crossings
* Road infrastructure impact

### 6. Machine Learning Results

* Model comparison
* ROC-AUC analysis
* Feature importance

### 7. Forecasting

* 12-month projected accident trend
* Confidence intervals
* Seasonal risk pattern

### 8. Live Predictions

* Real-time risk scoring
* Probability thresholds
* High-risk / low-risk classification

---

## Tech Stack

### Data Engineering

* Python
* pandas
* NumPy

### Machine Learning

* scikit-learn
* LightGBM
* XGBoost
* CatBoost

### Visualization

* Matplotlib
* Power BI

### Cloud / Platform

* Microsoft Fabric
* Lakehouse architecture

---

## Repository Structure

```text
Analysis-of-US-accident/
│
├── 01_Bronze_Layer.ipynb
├── 02_Silver_Layer.ipynb
├── 03_Gold_Layer.ipynb
├── 04_EDA.ipynb
├── US_Accidents_Final_Training_&_Dashboard.ipynb
├── 05_Prophet_Forecast
├── US_Accidents_Prediction_Service.ipynb
├── requirements.txt
└── README.md
```

---

## How to Run

Install dependencies:

```bash
pip install -r requirements.txt
```

Run notebooks in order:

1. Bronze
2. Silver
3. Gold
4. EDA
5. ML pipeline
6. Prediction notebook

---

## Key Outcomes

* 500K accident records processed
* Production-style Medallion pipeline
* Star schema for analytical reporting
* CatBoost production model with strong class separation
* 12-month forecasting layer
* 8 interactive Power BI dashboards
* Microsoft Fabric deployment-ready structure

---

## Project Value

This project demonstrates practical capabilities across:

* Data engineering
* Analytical modeling
* Business intelligence
* Machine learning evaluation
* Forecasting
* Production-oriented architecture

---

## Author

**Mohammed Elhefnawy**

GitHub: https://github.com/MohammedElhefnawy
