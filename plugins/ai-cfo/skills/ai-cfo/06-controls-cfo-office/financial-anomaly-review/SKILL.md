---
name: financial-anomaly-review
description: Review transaction or ledger data for duplicates, threshold splitting, unusual timing, vendor changes, manual journals, and other investigation flags without alleging fraud.
---

# Financial Anomaly Review

## Purpose

Identify unusual or suspicious patterns in transactional or ledger data for further investigation.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- transaction or ledger data
- analysis period

## Optional inputs

- vendor master
- employee list
- approval thresholds
- known related parties

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

An anomaly is a review flag, not proof of fraud or error.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Check duplicate invoice numbers, amounts, dates, and bank details where available.
2. Identify round-number, weekend, out-of-hours, threshold-splitting, and unusual-frequency patterns.
3. Detect sudden vendor/customer behaviour changes.
4. Identify unusual manual journals and reversals.
5. Rank findings by financial significance and explain why each is unusual.
6. Do not label an anomaly as fraud without evidence.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- duplicate payments
- new vendor receiving large payments quickly
- payments just below approval thresholds
- manual journals posted late in the close
- repeated bank-account changes

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

- `internal-controls-review`
- `audit-readiness`
- `month-end-close-review`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
