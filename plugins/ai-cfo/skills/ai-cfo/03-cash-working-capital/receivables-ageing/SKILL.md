---
name: receivables-ageing
description: Analyse receivables by contractual due date, ageing bucket, customer concentration, dispute status, and collection priority. Use for AR ageing and collections questions.
---

# Receivables Ageing

## Purpose

Analyse outstanding customer balances, overdue risk, collection priorities, and concentration.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- AR ledger or ageing report
- as-of date

## Optional inputs

- customer credit terms
- collection notes
- dispute flags
- revenue by customer

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Age from contractual due date when available; otherwise disclose the fallback date used.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Validate invoice date, due date, customer, and outstanding balance.
2. Bucket invoices by age.
3. Calculate overdue amount and concentration.
4. Identify top overdue accounts.
5. Distinguish disputed, promised, and uncontacted balances where data exists.
6. Create a collections priority list.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- large balances with missing due dates
- credit notes or negative invoices distorting ageing
- single-customer concentration
- repeated partial payments
- material balances beyond normal credit terms

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

- `working-capital-analysis`
- `cash-forecast`
- `customer-profitability`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
