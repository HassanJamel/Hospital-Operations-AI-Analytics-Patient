<p align="center">
  <a href="https://www.kaggle.com/code/hassanjameelahmed/hospital-operations-ai-analytics-patient" target="_blank">
    <img src="hospital-operations-ai-insights.png" alt="hospital operations" width="500">
  </a>
</p>


# Hospital Operations AI Analytics & Patient Flow Forecasting

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/jupyter-notebook-orange.svg)](https://jupyter.org)
[![Plotly](https://img.shields.io/badge/plotly-dashboard-blue.svg)](https://plotly.com)
[![Kaggle](https://img.shields.io/badge/kaggle-ready-blue.svg)](https://www.kaggle.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🏥 Executive Summary

A comprehensive AI-powered analytics solution for hospital operations optimization, featuring end-to-end machine learning pipeline with time series forecasting (Prophet/ARIMA), patient admission prediction (XGBoost/Random Forest), and interactive Plotly visualizations. This project analyzes 2017-2024 hospital admission patterns and provides actionable forecasts through 2026 for resource allocation and capacity planning.

**Key Results:**
- **89% accuracy** in admission prediction
- **10-year demand projections** (2017-2026)
- **30% baseline admission rate** with critical department disparities
- **Statistically validated insights** (Mann-Whitney U, Kruskal-Wallis tests)

## 📊 Business Problem

Modern hospitals face mounting pressure to:
- Optimize patient flow while maintaining quality care
- Forecast resource needs 3-5 years ahead
- Reduce wait times across departments (20-40 min average)
- Improve patient satisfaction scores
- Balance admission rates with capacity constraints

**Our Solution:** A data-driven ML framework that predicts admission probabilities, forecasts patient volumes, identifies operational bottlenecks, and provides resource allocation strategies.

## 🗂️ Dataset

**Source:** `healthcare_analytics_patient_flow_data.csv`

Time-series hospital operations data with the following key features:

| Feature | Type | Description | Business Impact |
|---------|------|-------------|-----------------|
| Patient Id | String | Unique identifier | Patient tracking |
| Patient Admission Date | Date | Admission/Visit date | Time series analysis |
| Patient Admission Time | Time | Admission/Visit time | Peak hour analysis |
| Patient Gender | Categorical | Male/Female | Demographics |
| Patient Age | Numeric | Age in years | Resource planning |
| Patient Race | Categorical | Ethnic background | Equity analysis |
| Department Referral | Categorical | Specialty department | Capacity planning |
| Patient Admission Flag | Categorical | Admission/Not Admission | Target variable |
| Patient Satisfaction Score | Numeric | 0-10 rating | Quality metric |
| Patient Waittime | Numeric | Minutes waited | Operational KPI |

**Sample Statistics:**
- **Dataset Shape:** (1,077 records, 10 features)
- **Missing Values:** &lt; 1%
- **Date Range:** 2023-2024 (base), 2017-2026 (forecast horizon)
- **Departments:** 7 major specialties (General Practice, Orthopedics, Cardiology, etc.)

## 🎯 Methodology

### Four Pillars of Exploratory Data Analysis

#### 1. Data Composition & Understanding
- Missing value analysis with interactive visualizations
- Data dictionary with business impact assessment
- Demographic distribution (age, gender, race)

#### 2. Data Distribution Analysis
- Wait time distribution (20-40 min cluster)
- Department performance metrics
- Patient satisfaction scores (0-10 scale)

#### 3. Data Relationships & Correlations
- **Correlation Matrix:** Wait time ↔ Satisfaction (-0.45)
- **Statistical Tests:** Mann-Whitney U Test (p &lt; 0.001)
- **Department Efficiency Matrix:** Admission rate vs. wait time

#### 4. Data Comparison
- **Department Benchmarking:** Cardiology (78% admission) vs. Orthopedics (45%)
- **Temporal Trends:** Monthly/quarterly patterns
- **Resource Allocation:** Bottleneck identification

### Machine Learning Models

#### Time Series Forecasting
- **Prophet Model:** Daily patient volume forecasting
- **ARIMA:** Statistical baseline for trend validation
- **Forecast Horizon:** 2017-2026 (10 years)
- **Components:** Trend, seasonality, holidays

#### Classification Models
- **XGBoost:** Primary model for admission prediction
- **Random Forest:** Ensemble validation
- **Logistic Regression:** Baseline comparison
- **Metrics:** ROC-AUC, Classification Report, Cross-validation

#### Feature Engineering
- Time components (year, month, day, hour, day-of-week)
- Department encoding
- Age binning
- Wait time percentiles

## 🙏 Acknowledgments

- **Dataset Source:** `healthcare_analytics_patient_flow_data.csv`
- **Libraries:** Pandas, Plotly, Prophet, XGBoost, Scikit-learn
- **Inspiration:** Healthcare AI Analytics Community

## 📞 Contact

**Project Link:** https://www.kaggle.com/hassanjameelahmed


