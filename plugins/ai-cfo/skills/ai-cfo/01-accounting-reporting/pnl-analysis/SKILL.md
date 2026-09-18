---
name: pnl-analysis
description: Analyse an income statement to explain revenue, cost, margin, EBITDA or EBIT, tax, and net-income performance. Use for P&L trends, variances, drivers, and earnings-quality questions.
---

# P&L Analysis

## Purpose

Analyse revenue, costs, margins, operating expenses, EBITDA/EBIT, tax, and net income to explain performance and identify material drivers.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- income statement or P&L
- analysis period
- currency and units

## Optional inputs

- budget or prior period
- revenue segmentation
- cost centre detail
- one-off item notes

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Use gross profit, gross margin, EBITDA/EBIT, and net margin only when the source statement supports those definitions. State any normalisation.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Reconcile revenue, gross profit, operating profit, and net income to source totals.
2. Calculate growth and margin percentages where comparable periods exist.
3. Separate volume, price, mix, cost, and one-off effects when data permits.
4. Identify the largest positive and negative movements by absolute and percentage impact.
5. Assess operating leverage and whether margin movement is structural or temporary.
6. Summarise the 3 to 5 most material drivers.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- revenue growth with deteriorating gross margin
- EBITDA growth caused mainly by one-off credits
- large unexplained 'other income' or 'other expense'
- cost lines growing materially faster than revenue
- positive profit with weak or negative operating cash flow

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

- `budget-vs-actual`
- `cash-flow-analysis`
- `management-commentary`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
