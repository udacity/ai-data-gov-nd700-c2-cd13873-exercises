# M006 — Fraud Detection System: Fact Sheet

Use these facts to complete M006's Model Card. These are the measured values and
known attributes handed over by the engineering team — you should not need to
invent any of them.

## Model Details
- **Model ID:** M006
- **Model Name:** Fraud Detection System
- **Version:** 4.2.0
- **Model Type:** Anomaly Detection
- **Framework:** Isolation Forest + Neural Network
- **Developers:** David Lee, Security Team
- **Department:** Security
- **Date Created:** 2021-09-10
- **Last Updated:** 2024-12-05
- **Owner:** David Lee

## Intended Use
- **Primary purpose:** Detect fraudulent transactions and chargebacks in real-time
- **Primary users:** Fraud analysts, transaction processing systems

## Training Data
- **Sources:** 12 months of transaction data, chargeback reports, dispute resolution records, device fingerprinting data
- **Size:** 500M transactions, 50K confirmed fraud cases
- **Preprocessing:** PII anonymization, feature engineering for transaction patterns, handling class imbalance (0.01% fraud rate), normalization of amounts across currencies
- **Known quality issues:** Severe class imbalance; some fraud cases mislabeled or discovered late

## Performance Metrics (measured)
- **Precision:** 0.89
- **Recall:** 0.76
- **F1 score:** 0.82
- **AUC-ROC:** 0.94
- **Average latency:** 120 ms
- **False positive rate:** 2.1%

## Bias Test Results (measured)
- **Testing performed across:** geographic fairness, customer demographics impact, transaction amount distribution
- **Known issues:** higher false positive rates for international transactions; age group 65+ flagged at higher rate
- **Demographic variation:** within 3.2% false positive rate across regions; within 4.8% across age groups
- **Geographic variance:** ±3.2%
- **Demographic variance:** ±4.8%

---

**Left for you to reason through (not provided — these are your governance judgments):**
out-of-scope uses, known limitations & failure modes, edge cases, bias mitigation
strategy, and the monitoring & update plan.