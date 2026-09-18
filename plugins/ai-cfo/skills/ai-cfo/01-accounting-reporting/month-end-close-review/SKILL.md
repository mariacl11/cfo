---
name: month-end-close-review
description: Review a month-end close for reconciliation gaps, unsupported balances, cut-off issues, accruals, and unusual journals. Use for close exception review, not audit assurance.
---

# Month-End Close Review

## Purpose

Review whether a period close is complete, internally consistent, and ready for management reporting.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- trial balance or general ledger
- close period
- entity list

## Optional inputs

- bank reconciliations
- AR/AP subledgers
- fixed asset register
- accrual schedules
- intercompany balances

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

A close review is an exception review. Do not imply audit assurance.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Confirm all expected ledgers and entities are included.
2. Review bank, AR, AP, payroll, tax, fixed asset, and intercompany reconciliations.
3. Inspect unusual or late journal entries.
4. Check accruals, prepayments, cut-off, and recurring entries.
5. Identify unreconciled accounts and unsupported balances.
6. Produce a close exceptions list with owners and priority.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- manual journals posted after reporting cut-off
- unreconciled bank or control accounts
- large suspense balances
- material negative AR/AP items
- missing intercompany eliminations

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

- `financial-anomaly-review`
- `audit-readiness`
- `monthly-mis`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
