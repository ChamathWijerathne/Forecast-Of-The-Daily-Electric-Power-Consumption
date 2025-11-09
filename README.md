# Electric Power Consumption — Time Series Analysis Project

## Overview

This repository contains our **group project** on time-series analysis using the **UCI/Kaggle Individual Household Electric Power Consumption Dataset**.  
The project involves weekly submissions including exploratory data analysis, time-series decomposition, autocorrelation analysis, forecasting preparation, and later model development.

The dataset records measurements of electric power consumption in one household with a one-minute sampling rate over several years.  
We aim to analyze consumption trends, seasonal patterns, and forecast future demand using classical and modern time series techniques.

---

## 👥 Group Members / Contributors

- [**Chamath Wijerathne**](https://github.com/ChamathWijerathne)  
- [**Nada Rahali**](https://github.com/NadaRahali)  
- [**Tanjuma Haque**](https://github.com/tanjuma)

---

## 📁 Repository Structure

```
Forecast-Of-The-Daily-Electric-Power-Consumption/
├── docs/ # Weekly PDF reports
│ ├── week-01-report.pdf
├── notebooks/ # Weekly Jupyter notebooks
│ ├── eda.ipynb
├── requirements.txt # Python dependencies
├── .gitignore # Ignored files and folders
├── README.md # Project documentation
```

> 🗒️ *Note:* The `docs/` folder contains reports in PDF format, while `notebooks/` holds the corresponding `.ipynb` notebooks.  
> Both are updated weekly with new analysis cells and results.

---

## Project Objectives  
1. Perform **exploratory data analysis (EDA)** to understand trends, distributions, and missing values.  
2. Conduct **time-series decomposition** to identify trend, seasonality, and residual components.  
3. Perform **autocorrelation analysis** to understand temporal dependencies.  
4. Design a **data partitioning strategy** for robust model training and validation.  
5. Build and evaluate **forecasting models** (later weeks).  
6. Document progress weekly through notebooks and reports.

---

## 🗓️ Weekly Deliverables  

| Week | Task Description | Deliverables |
|------|------------------|--------------|
| **Week 1** | Time-series visualization, EDA, STL decomposition, autocorrelation, and partitioning plan | `week-01-eda.ipynb` + `week-01-report.pdf` |

---

## 📊 Dataset Information  

**Source:** [Kaggle - Individual Household Electric Power Consumption Data Set](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set)  
**Description:**  
This dataset contains measurements of electric power consumption in a single household with a 1-minute sampling rate over almost 4 years.

**Main Columns Used:**
| Column | Description | Unit |
|---------|-------------|------|
| `Global_active_power` | Household global minute-averaged active power | kilowatts (kW) |
| `Global_reactive_power` | Global reactive power | kilowatts (kW) |
| `Voltage` | Average voltage | volts (V) |
| `Global_intensity` | Average current intensity | amperes (A) |
| `Sub_metering_1/2/3` | Energy sub-metered in different areas | watt-hours (Wh) |

---

## Environment Setup  

### Create & Activate a Virtual Environment  
```bash
# Create environment
python -m venv .venv

# Activate (Linux/macOS)
source .venv/bin/activate

# Activate (Windows)
.venv\Scripts\activate

All notebooks were developed using Python 3.10+ with the following key libraries:

pip install -r requirements.txt
