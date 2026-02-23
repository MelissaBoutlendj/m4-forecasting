# M4 Time Series Forecasting Challenge – Quarterly Dataset

This project presents a comprehensive benchmarking study of time series
forecasting methods applied to the **M4 Competition – Quarterly subset**.
We compare classical statistical models, machine learning approaches,
and deep learning architectures under a unified experimental protocol.

The objective is to evaluate the strengths, limitations, and trade-offs
of each modeling family when forecasting multiple univariate
quarterly time series.

---

## Project Objectives

- Forecast quarterly time series with a fixed horizon of **8 steps**
- Compare **statistical, ML, and DL models** on the same dataset
- Evaluate performance using **official M4 metrics**:
  - sMAPE (Symmetric Mean Absolute Percentage Error)
  - MASE (Mean Absolute Scaled Error)
- Analyze **robustness, interpretability, and computational cost**
- Provide an academically rigorous and reproducible benchmark

---

## Dataset

- **Source**: M4 Forecasting Competition
- **Subset**: Quarterly
- **Characteristics**:
  - Univariate time series
  - Heterogeneous lengths
  - Clear seasonal patterns (period = 4)
- **Forecast horizon**: 8 quarters
- **Scope of study**: up to **100 series**

---

## Methodology Overview

The project follows a structured pipeline:

### Data Preparation
- Conversion from **wide to long format**
- Handling of artificial missing values
- Temporal indexing with quarterly frequency
- Chronological train/test split (no shuffling)

### Exploratory Analysis
- Raw visualization of representative series
- Seasonal decomposition (trend, seasonality, residuals)
- Stationarity testing (ADF)
- Differencing when required
- ACF / PACF analysis

### Statistical Models
- ARIMA
- SARIMA (seasonal extension)
- Parameter identification and residual diagnostics

### Machine Learning
- Feature engineering:
  - Lag features
  - Rolling statistics
  - Seasonal indicators
- Models:
  - Linear regression (regularized)
  - Random Forest
  - Gradient Boosting / XGBoost

### Deep Learning
- MLP
- LSTM networks
- Transformer-based architectures
- Sequence-to-sequence forecasting

### Evaluation & Comparison
- Metrics computed **per series**
- Aggregated results over 100 series
- Distribution analysis (boxplots, histograms)
- Stability and robustness assessment

---

## Evaluation Metrics

### 🔹 sMAPE
Symmetric Mean Absolute Percentage Error  
Robust to scale differences across series.

### 🔹 MASE
Mean Absolute Scaled Error  
Normalized against a naïve baseline, allowing fair comparison
across heterogeneous time series.

---
