# Lesson 3: AI Risk Assessment

## Overview

This lesson covers AI risk assessment frameworks using the NIST AI Risk Management Framework (AI RMF). Students learn to identify, categorize, and score risks across the four NIST functions (Govern, Map, Measure, Manage), build risk registers, and visualize risk profiles using Python. The exercise includes producing an executive summary of risk findings.

## File Structure

```
lesson-3-ai-risk-assessment/
├── demo/
│   ├── risk_assessment_demo.xlsx          # Partially pre-filled (instructor fills live)
│   ├── risk_assessment_demo_solution.xlsx # Completed version (instructor reference)
│   └── risk_scoring_demo.ipynb            # Notebook walkthrough for risk visualization
├── exercises/
│   ├── starter/
│   │   ├── risk_assessment.xlsx           # Student starting file (with hints)
│   │   └── risk_scoring.ipynb             # Notebook with TODO placeholders
│   └── solution/
│       ├── risk_assessment.xlsx           # Completed solution
│       └── risk_scoring.ipynb             # Completed notebook
└── README.md
```

## Demo

**Scenario: CareBot Health** — A hospital network operating DiagnosAI, a clinical decision-support system that recently had a near-miss drug interaction incident.

The instructor populates a risk register live with 5 risks across NIST AI RMF functions, scoring them by likelihood and impact, and calculating overall risk levels. The notebook demonstrates how to visualize risk scores with a heat map (color-coded by risk category) and generate summary statistics.

## Exercise

**Scenario: FinGuard AI** — A fintech company (400 employees) whose FraudShield fraud detection system has been flagged for socioeconomic bias, disproportionately flagging transactions from lower-income zip codes.

### Task

**Part 1 — Risk Register (Excel)**

1. **Risk Identification** — Identify 15 risks across all four NIST AI RMF functions (Govern, Map, Measure, Manage). Three sample risks are pre-filled to demonstrate the expected format and detail level.
2. **Risk Scoring** — For each risk, assign likelihood (1–5) and impact (1–5) scores using the provided Scoring Rubric sheet, then calculate the risk level (Critical / High / Medium / Low).
3. **Mitigation Planning** — Specify a mitigation strategy, responsible owner, and target date for each risk.

**Part 2 — Risk Visualization (Notebook)**

1. Load risk register data (3 pre-filled + 12 student-defined risks) into a pandas DataFrame and calculate risk scores (Impact × Likelihood).
2. Assign risk levels using thresholds: Critical (≥15), High (10–14), Medium (5–9), Low (<5).
3. Generate a ranked risk register sorted by score.
4. Create a risk heat map (Impact vs. Likelihood scatter plot, color-coded by risk category).
5. Build a grouped bar chart showing average and maximum risk score by category (Technical, Ethical, Legal, Operational).
6. Create a pie chart showing risk level distribution (Critical / High / Medium / Low).
7. Produce a formatted executive summary report with risk level breakdown, top 5 priority risks, and key findings.

### Color Guide

| Color | Cell Text | Meaning |
|-------|-----------|---------|
| Light blue | Pre-filled data | Pre-filled content — do not modify |
| Pink | Contains `[Your response here]` prompts | Your work area — fill these cells |
| Yellow | Contains reference text (read-only) | Reference material — do not edit |
| Green | Scenario description | Scenario brief context |

### Estimated Time

~30 minutes
