# M002 — Demand Forecasting: Fact Sheet

Use these facts to complete M002's Model Card. These are the measured values and
known attributes handed over by the engineering team — you should not need to
invent any of them.

## Model Details
- **Model ID:** M002
- **Model Name:** Demand Forecasting
- **Version:** 1.8.0
- **Model Type:** Time Series ML
- **Framework:** ARIMA + XGBoost ensemble
- **Developers:** Marcus Johnson, Data Science Team
- **Department:** Supply Chain
- **Date Created:** 2022-03-20
- **Last Updated:** 2024-11-28
- **Owner:** Marcus Johnson

## Intended Use
- **Primary purpose:** Predict product demand for inventory optimization
- **Primary users:** Supply chain managers and inventory planners

## Training Data
- **Sources:** 24 months of historical sales data, seasonal indicators, marketing campaign calendar, inventory levels
- **Size:** 24 months × 5,000 SKUs = 120K time series
- **Preprocessing:** Detrending, seasonal decomposition, outlier detection and smoothing, feature engineering for lag variables
- **Known quality issues:** Some SKUs have gaps during stockouts; promotional spikes create anomalies

## Performance Metrics (measured)
- **MAPE:** 8.3% (Mean Absolute Percentage Error)
- **RMSE:** 45 units
- **Forecast accuracy (30d):** 92.1%
- **Forecast accuracy (90d):** 87.5%

## Bias Test Results (measured)
- **Testing performed across:** product category, regional demand variation, seasonal fairness
- **Demographic/segment variation:** within 12% accuracy across product categories; within 8% accuracy across geographic regions
- **Category variation:** ±12%
- **Regional variation:** ±8%

---

**Left for you to reason through (not provided — these are your governance judgments):**
out-of-scope uses, known limitations & failure modes, edge cases, bias mitigation
strategy, and the monitoring & update plan.
