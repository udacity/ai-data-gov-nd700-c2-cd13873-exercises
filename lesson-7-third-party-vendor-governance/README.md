# Lesson 7: Third-Party Vendor Governance

## Overview

This lesson covers third-party vendor governance for AI systems, including vendor risk scoring, SLA compliance monitoring, and vendor evaluation frameworks. Students learn to assess vendor risk across multiple dimensions (security, data handling, transparency, financial stability, SLA quality), generate recommendations, and build compliance dashboards.

## File Structure

```
lesson-7-third-party-vendor-governance/
├── demo/
│   ├── vendor_governance_demo.xlsx              # Partially pre-filled (instructor fills live)
│   ├── vendor_governance_demo_solution.xlsx      # Completed version (instructor reference)
│   ├── vendor_risk_scoring_demo.ipynb            # Notebook walkthrough for vendor risk scoring
│   └── vendor_comparison_demo.png                # Generated visualization (demo output)
├── exercises/
│   ├── starter/
│   │   ├── vendor_governance_starter.xlsx        # Student starting file (with hints)
│   │   └── vendor_risk_scoring_starter.ipynb     # Notebook with TODO placeholders
│   └── solution/
│       ├── vendor_governance_solution.xlsx        # Completed solution
│       ├── vendor_risk_scoring_solution.ipynb     # Completed notebook
│       ├── vendor_risk_comparison.png             # Generated visualization (solution output)
│       ├── vendor_radar.png                       # Generated visualization (solution output)
│       └── sla_compliance_dashboard.png           # Generated visualization (solution output)
└── README.md
```

## Demo

**Scenario: CloudFirst Financial** — A financial services company evaluating 2 AI vendors (CloudVault AI and TitanScale AI) for their fraud detection system after a competitor suffered a 6-hour vendor outage.

The instructor walks through vendor governance concepts live, filling in vendor assessment criteria and risk scores. The notebook demonstrates the full workflow for 2 vendors (CloudVault AI and TitanScale AI): defining evaluation scores across 5 criteria, calculating weighted risk scores (1–5 scale) using predefined weights, generating 30 days of simulated SLA data, analyzing uptime and latency compliance, producing a side-by-side comparison chart, and generating governance recommendations.

## Exercise

**Scenario: InsureLogic AI** — An insurance technology company managing 5 AI vendor relationships (NovaMind API, CloudVault AI, TitanScale AI, DeepLens AI, SafeGuard AI) for claims processing, fraud detection, and customer service. A vendor model update recently caused false claim denials, triggering a formal risk assessment.

### Task

**Part 1 — Vendor Governance (Excel)**

1. **Vendor Assessment** — Evaluate each vendor across security posture, data handling practices, model transparency, financial stability, and SLA compliance. Document certifications, evidence, and risk ratings.
2. **SLA Monitoring** — Track vendor SLA performance including uptime, latency, and incident response metrics against contractual thresholds.

**Part 2 — Vendor Risk Scoring (Notebook)**

Vendor evaluation scores (0–100 per criterion) and 30 days of simulated SLA data are provided inline for all 5 vendors.

1. **Define Scoring Weights** — Assign weights across 6 risk dimensions (Security, Data Handling, Transparency, Financial Stability, SLA Compliance, Exit Strategy) that sum to 1.0, reflecting insurance-industry priorities.
2. **Calculate Risk Scores** — Implement a function that computes a weighted average of vendor scores and converts to a 1–5 risk scale using the formula: `risk = 5 - (weighted_score / 100) * 4`.
3. **Vendor Recommendation Logic** — Implement a function that classifies vendors as Highly Recommended (risk ≤ 1.5 + SLA compliant), Recommended (≤ 2.5 + SLA compliant), Acceptable with Monitoring (≤ 3.5), or Not Recommended (> 3.5).
4. **Visualizations** (pre-provided, run and review) — Risk comparison bar chart, 30-day SLA compliance dashboard (uptime + latency tracking), and radar chart comparing top 3 vendors across all dimensions.
5. **Final Assessment Report** — Review the ranked vendor summary with risk scores, SLA compliance status, and governance recommendations.

### Color Guide

| Color | Cell Text | Meaning |
|-------|-----------|---------|
| Light blue | Pre-filled data | Pre-filled content — do not modify |
| Pink | Contains `[Your response here]` prompts | Your work area — fill these cells |
| Yellow | Contains reference text (read-only) | Reference material — do not edit |
| Green | Scenario description | Scenario brief context |

### Estimated Time

~30 minutes
