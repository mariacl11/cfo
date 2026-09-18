---
name: revenue-forecast
description: Forecast revenue using operational drivers such as customers, conversion, churn, price, volume, mix, seasonality, and timing. Use for forward revenue planning.
---

# Revenue Forecast

## Purpose

Forecast revenue using the most appropriate operational drivers and clearly stated assumptions.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- historical revenue
- forecast horizon
- revenue model

## Optional inputs

- sales pipeline
- customer cohorts
- pricing
- volumes
- renewals
- churn

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Prefer operational drivers to top-down growth rates. State conversion, churn, price, and volume assumptions where used.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Identify the business revenue model.
2. Choose driver-based forecasting where possible.
3. Separate existing-customer, new-customer, expansion, churn, price, and volume effects as applicable.
4. Model seasonality and timing.
5. Produce base forecast and key assumptions.
6. Back-test or sanity-check against historical conversion and growth.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- forecast based only on management target with no driver support
- pipeline counted at 100% without probability or conversion logic
- churn omitted from recurring revenue models
- capacity constraints ignored

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

- `rolling-forecast`
- `scenario-analysis`
- `sensitivity-analysis`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
