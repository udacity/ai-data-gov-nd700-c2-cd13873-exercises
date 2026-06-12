# M001 — Product Recommendation Chatbot: Fact Sheet

Use these facts to complete M001's Model Card. These are the measured values and
known attributes handed over by the engineering team — you should not need to
invent any of them.

## Model Details
- **Model ID:** M001
- **Model Name:** Product Recommendation Chatbot
- **Version:** 2.3.1
- **Model Type:** Generative AI (Large Language Model)
- **Framework:** GPT-4 with fine-tuning
- **Developers:** Sarah Chen, ML Team
- **Department:** E-Commerce
- **Date Created:** 2023-06-15
- **Last Updated:** 2024-12-15
- **Owner:** Sarah Chen
- **License:** Proprietary (internal use only)

## Intended Use
- **Primary purpose:** Real-time product recommendations via a conversational interface on the e-commerce platform
- **Primary users:** Retail customers browsing the e-commerce website

## Training Data
- **Sources:** Product catalog (50K products), historical customer purchase data, search logs, product reviews
- **Size:** ~2M customer interactions, 50K product records, 100K reviews
- **Preprocessing:** Text cleaning, tokenization, product embeddings, PII removal, missing-value handling
- **Known quality issues:** Some products have sparse review data; older reviews may contain biased language

## Performance Metrics (measured)
- **BLEU score:** 0.72 (relevance of recommendations)
- **CTR improvement:** +18% vs. baseline
- **Latency p50:** 450 ms
- **Latency p95:** 800 ms
- **Revenue improvement:** +12%
- **Satisfaction improvement:** +8%
- **Coverage:** 95% of queries return recommendations

## Bias Test Results (measured)
- **Testing performed across:** gender, racial/ethnic representation, socioeconomic, age
- **Demographic performance variation:** within 3% recall across gender (M/F/Other); within 5% recall across age groups
- **Disparate impact ratio:** 0.92
- **Prediction parity:** 0.89

---

**Left for you to reason through (not provided — these are your governance judgments):**
out-of-scope uses, known limitations & failure modes, edge cases, bias mitigation
strategy, and the monitoring & update plan.
