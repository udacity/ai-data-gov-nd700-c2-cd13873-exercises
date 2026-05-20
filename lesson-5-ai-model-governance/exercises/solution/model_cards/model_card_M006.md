# Model Card: Fraud Detection System

**Model ID**: M006 | **Version**: 4.2.0

## Model Details

- **Model Name**: Fraud Detection System
- **Model ID**: M006
- **Version**: 4.2.0
- **Model Type**: Anomaly Detection
- **Framework**: Isolation Forest + Neural Network
- **Developers**: David Lee, Security Team
- **Department**: Security
- **Date Created**: 2021-09-10
- **Last Updated**: 2024-12-05
- **Owner**: David Lee

## Intended Use

### Primary Purpose
Detect fraudulent transactions and chargebacks in real-time

### Primary Users
Fraud analysts, transaction processing systems

### Out-of-Scope Uses
- Customer credit scoring
- Behavioral profiling
- Identity verification

## Training Data

### Data Sources
- 12 months of transaction data
- Chargeback reports
- Dispute resolution records
- Device fingerprinting data

### Data Size
500M transactions, 50K confirmed fraud cases

### Preprocessing
- PII anonymization
- Feature engineering for transaction patterns
- Handling class imbalance (0.01% fraud rate)
- Normalization of amounts across currencies

### Data Quality Issues
Severe class imbalance; some fraud cases not yet labeled

## Performance Metrics

- **Precision**: 0.89
- **Recall**: 0.76
- **F1 Score**: 0.82
- **Auc Roc**: 0.94
- **Avg Latency**: 120ms
- **False Positive Rate**: 2.1%

## Ethical Considerations & Bias Testing

### Bias Testing Conducted
- Geographic fairness analysis
- Customer demographics impact
- Transaction amount distribution

### Known Bias Issues
- Higher false positive rates for international transactions
- Age group 65+ flagged at higher rate

### Demographic Performance Variation
- **Geographic**: Within 3.2% false positive rate across regions
- **Age Group**: Within 4.8% false positive rate across age groups

### Fairness Metrics
- **Geographic Variance**: ±3.2%
- **Demographic Variance**: ±4.8%

### Mitigation Strategies
- Geographic calibration of thresholds
- Age-aware fraud scoring
- Regular fairness audits

## Limitations & Failure Modes

### Known Limitations
- Cannot detect never-before-seen fraud patterns
- High false positive rate impacts customer experience
- Requires labeled fraud data for retraining

### Failure Modes
- False positives block legitimate transactions
- Sophisticated fraud may bypass anomaly detection

### Edge Cases
- Large legitimate purchases
- International business travel
- New customer first transaction

## Recommendations & Monitoring

### Monitoring Plan
Real-time fraud rate monitoring; Daily false positive analysis; Monthly performance review

### Update Schedule
Weekly retrain with new fraud data; Quarterly model evaluation

### Next Review Date
2025-03-05
