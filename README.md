# Demand Forecasting for 6 SKUs using Time Series Models

This project focuses on forecasting weekly demand for six SKUs using various time series models. The goal is to predict demand for the next 4 weeks and select the best model per SKU based on MAPE.

## 🎯 Objective

- Forecast 4 weeks of demand for 6 SKUs  
- Evaluate and compare models using **MAPE** (Mean Absolute Percentage Error)

## 📂 Dataset Overview

- Format: Excel file with 6 sheets (one per SKU)
- Frequency: Weekly aggregated transaction data  
- Target variable: `QTY`  
- Ignored columns: `Cat-III Desc`, `Cat-IV Desc`, `Net Sales`

## 🛠️ Tools & Techniques

- **Language:** Python  
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `statsmodels`, `openpyxl`
- **Data Cleaning:**  
  - Missing values handled via **interpolation**
- **Models Evaluated:**  
  - Naive Forecast  
  - Simple Exponential Smoothing  
  - Holt’s Linear Trend Method  
  - Holt-Winters Exponential Smoothing (**Multiplicative Model**)  
  - ARIMA / SARIMA (where applicable)  
- **Evaluation Metric:**  
  - **MAPE**, tested on the last 3 weeks of each SKU

## 🔁 Workflow

1. Load and clean data from all 6 sheets
2. Interpolate missing values
3. Apply multiple time series models to each SKU
4. Forecast 4 future weeks
5. Evaluate using MAPE and select the best model per SKU

## 📊 Results Summary

- Each SKU was modeled independently
- Best-performing model selected based on lowest MAPE
- All selected models achieved **MAPE < 10%**

## ✅ Conclusion

- No single model was best for all SKUs  
- Holt-Winters (multiplicative) was highly effective in most cases  
- Model selection based on MAPE ensures reliable forecasts for inventory planning

## 👨‍💻 Author

**Aman Raj**  
Final Year Engineering Student | Data Science Enthusiast  
GitHub: [amanraj-creator](https://github.com/amanraj-creator)
