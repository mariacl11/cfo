---
name: cfo-decision-memo
description: Produce a finance decision memo comparing viable options, quantified economics, cash and downside effects, risks, recommendation conditions, and monitoring triggers.
---

# CFO Decision Memo

## Purpose

Answer a management decision with quantified financial options, scenarios, risks, guardrails, and a clear finance recommendation.

## Use this skill when

Use this skill when the user asks for analysis that substantially matches the purpose above, or when the AI CFO orchestrator routes a broader task here.

## Do not use this skill when

- the task is primarily legal, tax-law, audit-opinion, or investment-advice work requiring a licensed professional
- the necessary source data is unavailable and the answer would require invented figures
- another specialist skill is clearly more direct and complete for the user's question

## Required inputs

- decision question
- relevant financial data

## Optional inputs

- strategic constraints
- risk tolerance
- timing
- alternatives

## Supported files

- XLSX / XLS
- CSV / TSV
- PDF financial statements or management reports
- ERP / accounting exports
- Plain-text tables

## Definitions and calculation logic

A recommendation must be explicitly tied to quantified evidence, assumptions, and decision constraints.

Before interpreting inputs, follow `../../docs/supported-files.md`, including its source-trust rules. Follow `../../docs/calculations.md` for common formulas and ratio conventions.

Every material output figure must be identifiable as:
- **Reported**
- **Calculated**
- **Assumption**
- **AI interpretation**

## Workflow

1. Define the decision precisely.
2. State the current financial position relevant to the decision.
3. Quantify each viable option.
4. Model cash, profitability, and downside where relevant.
5. Identify assumptions and risks.
6. Provide a finance recommendation tied to explicit conditions.
7. Define metrics and triggers to monitor after the decision.

## Validation checks

Before concluding:

1. Confirm entity, period, currency, and units.
2. Check source totals and internal arithmetic.
3. Confirm actual, budget, forecast, and prior-period data are not mixed.
4. Check for duplicate rows, missing values, or inconsistent date ranges where relevant.
5. Recalculate material ratios from source data.
6. Flag any conclusion that changes materially under a reasonable alternative assumption.

## Red flags

- recommendation unsupported by numbers
- only one option analysed when alternatives exist
- cash impact omitted
- assumptions presented as facts

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

- `scenario-analysis`
- `business-case-analysis`
- `cash-forecast`

## Completion criteria

This skill is complete when:
- the relevant calculations are traceable
- material drivers are identified
- inconsistencies are reconciled or flagged
- the output answers the user's finance question
- assumptions and data gaps are visible
