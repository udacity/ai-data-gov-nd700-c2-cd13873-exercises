# Lesson 4: ISO/IEC 42001 AI Management

## Overview

This lesson covers the ISO/IEC 42001:2023 AI management system standard — its structure, requirements, and certification pathway. Students learn to conduct gap analyses against ISO 42001 controls, assess organizational readiness across key control areas, and automate compliance documentation using Python and YAML.

## File Structure

```
lesson-4-iso-iec-42001-ai-management/
├── demo/
│   ├── iso42001_demo.xlsx                # Partially pre-filled (instructor fills live)
│   ├── iso42001_demo_solution.xlsx       # Completed version (instructor reference)
│   └── compliance_automation_demo.ipynb  # Notebook walkthrough for compliance automation
├── exercises/
│   ├── starter/
│   │   ├── iso42001_gap_analysis_starter.xlsx    # Student starting file (with TODO hints)
│   │   └── compliance_automation_starter.ipynb   # Notebook with TODO placeholders
│   └── solution/
│       ├── iso42001_gap_analysis_solution.xlsx   # Completed solution (with instructor comments)
│       └── compliance_automation_solution.ipynb  # Completed notebook
└── README.md
```

## Demo

**Scenario: NovaPharma AI** — A pharmaceutical company (800 employees) with two high-risk AI systems: DrugDiscoveryGPT (molecule screening for drug R&D) and ClinicalTrialOptimizer (patient cohort selection for clinical trials). They are pursuing ISO 42001 certification to satisfy regulatory and partner requirements.

The instructor walks through a gap analysis checklist live, assessing NovaPharma's current state against 10 key ISO 42001 controls across leadership, planning, support, operations, performance, and improvement. NovaPharma is presented as a more mature organization (existing AI governance charter, partial risk assessments) to contrast with the exercise scenario. The notebook demonstrates how to structure controls as Python dictionaries, calculate readiness scores, generate a gap analysis report, and produce YAML compliance documentation.

## Exercise

**Scenario: DataVault Analytics** — A data analytics company (350 employees) providing AI-powered business intelligence through InsightEngine (automated report writing) and AnomalyDetect (real-time financial anomaly detection). A recent incident where InsightEngine hallucinated financial figures in a client report has triggered an urgent push toward ISO 42001 certification.

### Task

**Part 1 — Gap Analysis (Excel)**

1. **Gap Analysis Checklist** — Assess DataVault's current state against 17 ISO 42001 controls spanning six control areas (Leadership & Policy, Planning, Support, Operations, Performance Evaluation, Improvement). For each control, evaluate the current implementation state, document available evidence, describe gaps, assign a readiness score (1–5), set priority, and define remediation actions.
2. **Readiness Dashboard** — Summarize readiness scores by control area, calculate overall certification readiness percentage, and determine whether DataVault meets the certification threshold (≥80%).

**Part 2 — Compliance Automation (Notebook)**

1. Define ISO 42001 control requirements as structured Python dictionaries across six control areas (3 pre-filled AI Policy controls + 14 student-defined controls across Planning, Support, Operations, Performance, and Improvement).
2. Convert the requirements dictionary into a flat pandas DataFrame and calculate per-area readiness scores with status classification (Ready / In Progress / Not Ready).
3. Generate a formatted gap analysis report with executive summary, per-area breakdown, and critical gaps (score ≤ 2).
4. Create YAML compliance documentation with company metadata, assessment results, and critical findings using `yaml.dump()`.
5. Build a Jinja2 template for generating a professional compliance summary document with an implementation roadmap.
6. Identify critical gaps, produce prioritized remediation recommendations with estimated effort levels, and summarize top actions.

### Color Guide

| Color | Cell Text | Meaning |
|-------|-----------|---------|
| Light blue | Pre-filled data | Pre-filled content — do not modify |
| Pink | Contains `[Your response here]` prompts | Your work area — fill these cells |
| Yellow | Contains reference text (read-only) | Reference material — do not edit |
| Green | Scenario description | Scenario brief context |

### Estimated Time

~30 minutes
