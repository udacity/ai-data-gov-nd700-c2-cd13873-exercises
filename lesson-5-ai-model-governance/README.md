# Lesson 5: AI Model Governance

## Overview

This lesson covers AI model governance practices, including model inventory management, Model Card generation (following the Google standard), and model lifecycle tracking. Students learn to define structured metadata, generate compliance documentation, and monitor model review schedules using Python and pandas.

## File Structure

```
lesson-5-ai-model-governance/
├── demo/
│   ├── model_governance_demo.xlsx              # Partially pre-filled (instructor fills live)
│   ├── model_governance_demo_solution.xlsx      # Completed version (instructor reference)
│   └── model_card_generator_demo.ipynb          # Notebook walkthrough for model card generation
├── exercises/
│   ├── starter/
│   │   ├── model_governance_starter.xlsx        # Student starting file (with hints)
│   │   └── model_card_generator_starter.ipynb   # Notebook with TODO placeholders
│   └── solution/
│       ├── model_governance_solution.xlsx        # Completed solution
│       ├── model_card_generator_solution.ipynb   # Completed notebook
│       └── model_cards/                          # Generated model card outputs
│           ├── model_card_M001.md
│           ├── model_card_M002.md
│           ├── model_card_M006.md
│           └── model_inventory.csv
└── README.md
```

## Demo

**Scenario: TechVault Solutions** — A B2B SaaS company providing cloud-based data management with a single AI model.

The instructor walks through model governance concepts live, filling in model inventory fields and governance lifecycle stages. The notebook demonstrates the full workflow for a single model (DocuMind AI — a document summarization LLM): defining structured metadata across all seven Google-standard Model Card sections, implementing a `generate_model_card_markdown()` function, generating and displaying the card, creating a one-model inventory DataFrame with lifecycle tracking, and analyzing review status to flag overdue or upcoming reviews.

## Exercise

**Scenario: RetailGenius** — An e-commerce company managing multiple AI models across departments.

### Task

**Part 1 — Model Governance (Excel)**

1. **Model Inventory** — Catalog AI models with metadata including model ID, name, version, type, framework, risk tier, lifecycle stage, and review schedule.
2. **Governance Dashboard** — Track model lifecycle stages, identify models overdue for review, and summarize governance compliance status.

**Part 2 — Model Card Generator (Notebook)**

1. Define structured metadata dictionaries for 2–3 AI models, including all seven Model Card sections (Model Details, Intended Use, Training Data, Performance Metrics, Ethical Considerations, Limitations, Recommendations & Monitoring).
2. Implement a `generate_model_card_markdown()` function that converts a metadata dictionary into a complete Markdown-formatted Model Card.
3. Generate Model Cards for all defined models and display them.
4. Build a model inventory DataFrame (5–8 models) tracking lifecycle stage, approval status, risk tier, owner, and review dates.
5. Calculate lifecycle metrics: days in current stage, days since last review, and days until next review.
6. Identify models overdue for review and models with upcoming reviews (within 30 days).
7. Create a summary dashboard with counts by lifecycle stage, risk tier, and approval status.
8. Export generated Model Cards as `.md` files and the inventory as CSV.

### Color Guide

| Color | Cell Text | Meaning |
|-------|-----------|---------|
| Light blue | Pre-filled data | Pre-filled content — do not modify |
| Pink | Contains `[Your response here]` prompts | Your work area — fill these cells |
| Yellow | Contains reference text (read-only) | Reference material — do not edit |
| Green | Scenario description | Scenario brief context |

### Estimated Time

~30 minutes
