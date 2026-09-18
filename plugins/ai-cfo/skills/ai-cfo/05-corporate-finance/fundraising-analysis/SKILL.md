---
name: fundraising-analysis
description: Determine funding need, timing, target runway, strategic buffer, use of funds, valuation assumptions, and dilution across fundraising scenarios.
---

# Fundraising Analysis

## Purpose

Estimate funding requirement, runway extension, dilution, and use-of-funds implications.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- current cash
- burn or forecast
- fundraising objective

## Optional inputs

- valuation assumptions
- cap table
- minimum cash buffer
- growth plan

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Separate pre-money and post-money valuation assumptions and model financing timing explicitly.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Calculate funding need based on forecast and target runway.
2. Separate operating requirement from strategic buffer.
3. Model timing of fund receipt.
4. Estimate dilution under user-provided valuation assumptions.
5. Show use of funds.
6. Compare smaller/larger raise scenarios and consequences.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- funding requirement based only on headline monthly burn
- fundraise assumed to close immediately
- minimum cash buffer ignored
- dilution calculated from inconsistent pre-money/post-money assumptions

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

- `cash-runway`
- `cash-forecast`
- `company-valuation`
- `scenario-analysis`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
