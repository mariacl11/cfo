---
name: business-case-analysis
description: Evaluate a proposed investment, hire, office, expansion, or initiative using incremental cash flows, payback, NPV or IRR, downside cases, and constraints.
---

# Business Case Analysis

## Purpose

Evaluate a proposed hire, product, office, campaign, system, expansion, or operational initiative financially.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- proposal
- costs
- expected benefits
- timing

## Optional inputs

- cash constraints
- alternatives
- strategic requirements
- risk assumptions

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Use incremental future cash flows. Exclude sunk costs from the go/no-go economics.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Define the decision and alternatives.
2. Separate one-time and recurring costs.
3. Quantify expected revenue, savings, or capacity benefits.
4. Build cash flows over the relevant horizon.
5. Calculate payback and, where appropriate, NPV/IRR.
6. Run downside and break-even cases.
7. Identify non-financial constraints separately.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- benefits counted without timing or probability
- sunk costs included as future decision costs
- working capital or implementation costs omitted
- strategic claim used as substitute for financial evidence

## Output format

### Executive Summary
Maximum 5 bullets. State the decision-useful findings first.

### Key Numbers
Use a compact table showing source, current value, comparator, and change where relevant.

### Analysis
Explain the main drivers, relationships, and financial implications.

### Risks / Red Flags
Prioritise by financial significance.

### Recommended Actions
Provide concrete CFO actions, not generic finance advice.

### Assumptions and Data Gaps
List every material assumption and missing input.

## Assumptions and uncertainty

- Never silently fill missing figures.
- Do not convert a management target into a forecast without saying so.
- If a calculation depends on an assumption, show the assumption beside the result.
- Where source data conflicts, prefer reconciliation over interpretation.
- If the remaining uncertainty could reverse the conclusion, state that explicitly.

## Related skills

- `investment-appraisal`
- `scenario-analysis`
- `cfo-decision-memo`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
