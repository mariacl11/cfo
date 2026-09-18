---
name: debt-analysis
description: Analyse debt instruments, interest, maturities, fixed and floating exposure, leverage, coverage, covenant headroom, refinancing, and liquidity risk.
---

# Debt Analysis

## Purpose

Assess debt structure, servicing burden, maturities, covenants, and refinancing risk.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- debt schedule
- interest rates
- maturities
- cash flow

## Optional inputs

- covenants
- security
- amortisation schedule
- base rate exposure

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Use the lender's covenant definitions where available rather than generic ratio definitions.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Map each debt instrument.
2. Calculate principal, interest, and maturity schedule.
3. Assess fixed versus floating-rate exposure.
4. Calculate key leverage and coverage metrics where meaningful.
5. Check covenant headroom if covenant definitions are available.
6. Identify refinancing and liquidity concentrations.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- large maturity wall
- covenant headroom narrowing
- interest burden rising faster than operating cash flow
- short-term borrowing funding long-term needs
- cash counted despite lender restrictions

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

- `cash-forecast`
- `cash-runway`
- `fundraising-analysis`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
