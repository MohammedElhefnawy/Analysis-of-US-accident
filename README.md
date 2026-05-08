# 🚦 US Accident Analysis Project  

## 📌 Overview  
This project analyzes **US traffic accident data** using a **Medallion architecture pipeline** (Bronze → Silver → Gold), applies **machine learning models** for severity prediction, and leverages **forecasting techniques** to predict future accident trends. Finally, insights are visualized in **Power BI dashboards** for decision-making.  

---

## 🏗️ Architecture  
The project follows the **Medallion Architecture**:  

- **Bronze Layer**: Raw accident data ingestion.  
- **Silver Layer**: Cleaned and transformed data (handling missing values, duplicates, normalization).  
- **Gold Layer**: Aggregated and enriched datasets ready for ML and BI.  

📊 *[Add pipeline diagram here]*  

---

## 🔍 Features  
- **Data Cleaning**: Handling missing values, duplicates, and outliers.  
- **Exploratory Analysis**: Accident trends by state, weather, time, and severity.  
- **Machine Learning**: Severity classification using CatBoost, XGBoost, and ensemble models.  
- **Forecasting**: Accident trend prediction with Prophet and ARIMA.  
- **Power BI Dashboards**: Interactive reports with filters (state, severity, weather).  

---

## ⚙️ Installation & Setup  
1. Clone the repository:  
   ```bash
   git clone https://github.com/MohammedElhefnawy/Analysis-of-US-accident.git
   cd Analysis-of-US-accident
