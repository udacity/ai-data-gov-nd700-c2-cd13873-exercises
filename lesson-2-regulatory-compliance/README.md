# Lesson 2: Regulatory Compliance

## Overview

This lesson focuses on understanding and implementing regulatory compliance for AI systems, with an emphasis on the EU AI Act. Students learn to classify AI systems by risk tier, build compliance matrices, and document conformity evidence. A Python notebook reinforces the risk classification process programmatically.

## File Structure

```
lesson-2-regulatory-compliance/
├── demo/
│   ├── compliance_demo.xlsx              # Partially pre-filled (instructor fills live)
│   ├── compliance_demo_solution.xlsx     # Completed version (instructor reference)
│   └── eu_ai_act_classifier_demo.ipynb   # Notebook walkthrough for risk classification
├── exercises/
│   ├── starter/
│   │   ├── compliance_plan.xlsx          # Student starting file (with hints)
│   │   └── eu_ai_act_classifier.ipynb    # Notebook with TODO placeholders
│   └── solution/
│       ├── compliance_plan.xlsx          # Completed solution
│       └── eu_ai_act_classifier.ipynb    # Completed notebook
└── README.md
```

## Demo

**Scenario: AutoPilot Logistics** — A European logistics company operating RouteGenius (route optimization), WarehouseWatch (inventory monitoring), and HireBot (automated hiring), spanning three different EU AI Act risk tiers.

The instructor builds a compliance matrix live, classifying each system's risk tier, identifying applicable requirements, and documenting compliance gaps. The notebook demonstrates how to build a rule-based EU AI Act risk classifier in Python.

## Exercise

**Scenario: TalentScope AI** — An HR technology company whose recruitment screening tool uses video analysis for candidate assessment, with an 8% gender bias finding in recent audits.

### Task

**Part 1 — Compliance Plan (Excel)**

1. **Compliance Matrix** — For each of TalentScope's AI system requirements, determine the EU AI Act risk tier, identify applicable regulatory articles, document current control status (Implemented / Partial / Gap), and specify remediation actions for gaps.
2. **Conformity Evidence** — For each compliance requirement, document the evidence type, current status, responsible team, and target completion dates.

**Part 2 — Risk Classifier (Notebook)**

1. Define `RISK_TIERS` dictionary with descriptions, examples, and applicable articles for each EU AI Act tier (Unacceptable, High-Risk, Limited, Minimal).
2. Implement a `classify_ai_system()` function that evaluates boolean characteristics (biometric use, fundamental rights impact, safety criticality, social scoring, etc.) and returns a risk tier, applicable articles, required actions, and reasoning.
3. Define and classify 5 test AI systems spanning all four risk tiers (HR recruitment, healthcare diagnosis, entertainment chatbot, biometric finance, social scoring).
4. Generate a classification summary table and risk tier distribution.
5. Export classification results to CSV for compliance documentation.

### Color Guide

| Color | Cell Text | Meaning |
|-------|-----------|---------|
| Light blue | Pre-filled data | Pre-filled content — do not modify |
| Pink | Contains `[Your response here]` prompts | Your work area — fill these cells |
| Yellow | Contains reference text (read-only) | Reference material — do not edit |
| Green | Scenario description | Scenario brief context |

### Estimated Time

~30 minutes
