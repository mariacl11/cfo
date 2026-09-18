---
name: financial-statement-analysis
description: Produce an integrated analysis of the income statement, balance sheet, and cash-flow statement. Use when conclusions must be reconciled across all three financial statements.
---

# Financial Statement Analysis

## Purpose

Analyse P&L, balance sheet, and cash flow together to form an integrated view of financial health.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- P&L
- balance sheet
- cash flow statement
- period and currency

## Optional inputs

- budget
- prior periods
- notes to accounts
- debt schedules

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Treat the three statements as linked. A conclusion from one statement should be tested against the other two.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Validate all three statements and periods.
2. Analyse profitability and earnings quality.
3. Assess liquidity, working capital, leverage, and capital structure.
4. Assess cash conversion and free cash flow.
5. Identify inconsistencies between reported profit, balance-sheet movements, and cash.
6. Produce an integrated view of strengths, weaknesses, risks, and key questions.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- profits unsupported by cash
- rapid growth funded by deteriorating working capital
- debt growth without corresponding productive investment
- large unexplained accounting movements
- weak liquidity masked by non-cash assets

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

- `pnl-analysis`
- `balance-sheet-analysis`
- `cash-flow-analysis`
- `cfo-decision-memo`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
