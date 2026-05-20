# Lesson 9: AI Incident Management

## Overview

This lesson covers AI incident management, including incident playbook design, severity classification, threshold-based incident detection, escalation workflows, and post-incident review processes. Students learn to build comprehensive incident response frameworks for safety-critical AI systems using both structured Excel templates and Python-based monitoring logic.

## File Structure

```
lesson-9-ai-incident-management/
├── demo/
│   ├── incident_response_demo.xlsx              # Partially pre-filled (instructor fills live)
│   └── incident_response_demo_solution.xlsx      # Completed version (instructor reference)
├── exercises/
│   ├── starter/
│   │   ├── incident_detection_starter.ipynb      # Notebook with TODO placeholders
│   │   ├── incident_response_starter.xlsx        # Student starting file (with hints)
│   │   └── transitai_monitoring.png              # Generated visualization (starter output)
│   └── solution/
│       ├── incident_detection_solution.ipynb      # Completed notebook
│       ├── incident_response_solution.xlsx        # Completed solution
│       └── transitai_monitoring.png               # Generated visualization (solution output)
└── README.md
```

## Demo

**Scenario: RoutePilot AI** — A Series A logistics startup (3 cities, 500 active drivers, ~50,000 deliveries/day) building an AI-powered route optimization platform for delivery drivers.

The instructor walks through the workbook live, filling in incident response playbooks and severity classifications. The demo covers 3 sheets:

1. **Incident Playbook** — Build response plans for 3 incident types: route bias against certain neighborhoods (Bias), route accuracy degradation (Performance), and driver location data exposure (Security). For each incident, define severity level, detection method, initial response, and resolution steps.
2. **Severity Classification** — Review a 4-tier severity framework (S1 Critical through S4 Low) with response time SLAs ranging from < 15 minutes to < 24 hours.

## Exercise

**Scenario: TransitAI** — An urban transit company (15 metro areas, 2M+ daily passengers, 10,000+ vehicles) operating AI-powered autonomous route optimization and passenger communication for safety-critical transit operations.

### Task

**Part 1 — Incident Response (Excel)**

Students complete five governance deliverables across 5 sheets:

1. **Incident Playbook** — Build response plans for 10 incident types across 5 categories (Bias, Misuse, Performance, Security, Safety, Compliance). 5 incidents are pre-filled; students complete 5 remaining incidents (adversarial manipulation, training data poisoning, unauthorized access, and 2 others) with severity classification, detection methods, initial response, investigation steps, resolution steps, communication requirements, and post-resolution actions.
2. **Severity Classification** — Review the pre-filled 4-tier severity framework (S1–S4) with escalation requirements and communication scope for each level.
3. **Reporting Workflow** — Review a 10-step incident reporting workflow from detection through knowledge base updates. Steps 1–8 are pre-filled; students complete steps 9 (post-incident review) and 10 (knowledge base update) with responsible roles, timelines, and deliverables.
4. **Post-Incident Review** — Design a blameless post-incident review template with 9 review elements. 7 elements are pre-filled (timeline, root cause analysis, impact assessment, response effectiveness, lessons learned, preventive measures, action items); students complete 2 remaining elements (communication effectiveness and follow-up schedule).

**Part 2 — Incident Detection (Notebook)**

Using 100 hours of simulated TransitAI monitoring data with 7 injected anomalies, students implement threshold-based incident detection:

1. **Implement Detection Logic** — Complete the `detect_incidents()` function that compares 5 system metrics (model accuracy, response latency, bias score, error rate, data drift) against warning and critical thresholds, respecting the threshold direction (above/below).
2. **Implement Escalation Logic** — Complete the `determine_escalation()` function that routes incidents to appropriate teams based on severity (S1–S4) and metric type (e.g., security metrics escalate to CISO).
3. **Implement Response Recommendations** — Complete the `recommend_response()` function that suggests specific response actions based on the affected metric and severity level.
4. **Visualization** (pre-provided, run and review) — 5-panel monitoring dashboard showing metric values over time with warning/critical threshold lines and flagged incidents.

### Color Guide

| Color | Cell Text | Meaning |
|-------|-----------|---------|
| Light blue | Pre-filled data | Pre-filled content — do not modify |
| Pink | Contains `[Your response here]` prompts | Your work area — fill these cells |
| Yellow | Contains reference text (read-only) | Reference material — do not edit |
| Green | Scenario description | Scenario brief context |

### Estimated Time

~30 minutes
