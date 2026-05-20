# Model Card: Demand Forecasting

**Model ID**: M002 | **Version**: 1.8.0

## Model Details

- **Model Name**: Demand Forecasting
- **Model ID**: M002
- **Version**: 1.8.0
- **Model Type**: Time Series ML
- **Framework**: ARIMA + XGBoost Ensemble
- **Developers**: Marcus Johnson, Data Science Team
- **Department**: Supply Chain
- **Date Created**: 2022-03-20
- **Last Updated**: 2024-11-28
- **Owner**: Marcus Johnson

## Intended Use

### Primary Purpose
Predict product demand for inventory optimization

### Primary Users
Supply chain managers and inventory planners

### Out-of-Scope Uses
- Real-time price adjustment
- Marketing campaign planning
- Customer behavior prediction beyond demand

## Training Data

### Data Sources
- 24 months of historical sales data
- Seasonal indicators
- Marketing campaign calendar
- Inventory levels

### Data Size
24 months × 5,000 SKUs = 120K time series

### Preprocessing
- Detrending
- Seasonal decomposition
- Outlier detection and smoothing
- Feature engineering for lag variables

### Data Quality Issues
Some SKUs have gaps during stockouts; promotional spikes create anomalies

## Performance Metrics

- **Mape**: 8.3% (Mean Absolute Percentage Error)
- **Rmse**: 45 units
- **Forecast Accuracy 30D**: 92.1%
- **Forecast Accuracy 90D**: 87.5%

## Ethical Considerations & Bias Testing

### Bias Testing Conducted
- Category performance bias
- Regional demand variation
- Seasonal fairness

### Known Bias Issues
- Underforecasting for niche products
- Overforecasting during holiday season

### Demographic Performance Variation
- **Product Category**: Within 12% accuracy across all categories
- **Region**: Within 8% accuracy across geographic regions

### Fairness Metrics
- **Category Variation**: ±12% across categories
- **Regional Variation**: ±8% across regions

### Mitigation Strategies
- Category-specific models for niche products
- Holiday adjustment factors
- Regular retraining with latest data

## Limitations & Failure Modes

### Known Limitations
- Cannot predict unprecedented events (e.g., supply chain disruptions)
- Accuracy degrades for new products
- Relies on historical patterns that may change

### Failure Modes
- Zero forecast for discontinued products
- Sudden spikes due to marketing campaigns

### Edge Cases
- New product launches
- Competitor promotions
- Supply shortages

## Recommendations & Monitoring

### Monitoring Plan
Weekly accuracy checks; Monthly recalibration; Quarterly performance review

### Update Schedule
Monthly retraining; Quarterly model validation

### Next Review Date
2025-02-28
