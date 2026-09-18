---
name: financial-due-diligence
description: Perform analytical financial diligence on supplied data, covering revenue quality, normalized earnings, cash conversion, working capital, debt, commitments, and red flags.
---

# Financial Due Diligence

## Purpose

Review a target or business for earnings quality, cash conversion, working capital, debt, concentration, and financial red flags.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- historical financial statements
- transaction context

## Optional inputs

- monthly management accounts
- customer data
- AR/AP ageing
- debt schedule
- tax data

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

This is analytical diligence from supplied data, not an audit or assurance engagement.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Validate historical consistency.
2. Analyse revenue quality and concentration.
3. Normalise EBITDA and identify one-offs.
4. Assess cash conversion.
5. Assess working capital and seasonality.
6. Review debt and off-balance-sheet-like commitments from supplied data.
7. Create red-flag and follow-up request lists.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- customer concentration
- revenue recognised ahead of cash or delivery without explanation
- persistent EBITDA-to-cash gap
- large related-party balances
- unusual one-off adjustments
- working capital likely to create purchase-price pressure

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

- `financial-statement-analysis`
- `company-valuation`
- `working-capital-analysis`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
