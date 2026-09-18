---
name: cash-forecast
description: Build a period-by-period cash forecast using collection, payment, payroll, tax, capex, financing, and timing assumptions. Use to identify future liquidity gaps.
---

# Cash Forecast

## Purpose

Forecast opening cash, inflows, outflows, financing flows, and closing cash over a selected horizon.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- opening cash
- forecast horizon
- known cash inflows/outflows

## Optional inputs

- AR collections
- AP schedule
- payroll
- tax payments
- capex
- debt
- fundraising

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

Cash timing governs the forecast. Do not copy accrual revenue or expense timing directly unless payment timing is identical.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Build a period-by-period opening and closing cash schedule.
2. Model collections using expected cash timing rather than accounting revenue.
3. Model payroll, vendor, tax, capex, and financing payments separately.
4. Highlight minimum cash balance.
5. Identify liquidity gaps and timing risks.
6. Reconcile to any available P&L forecast.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- cash forecast copied directly from accrual P&L
- large receipts with no collection timing assumptions
- tax or debt service omitted
- negative cash balance without financing treatment

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

- `receivables-ageing`
- `payables-analysis`
- `cash-runway`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
