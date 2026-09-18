# Skill Format Standard

Every specialist `SKILL.md` should contain the following sections:

1. Skill
2. Purpose
3. Use this skill when
4. Do not use this skill when
5. Required inputs
6. Optional inputs
7. Supported files
8. Definitions and calculation logic
9. Workflow
10. Validation checks
11. Red flags
12. Output format
13. Assumptions and uncertainty
14. Related skills
15. Completion criteria

Every `SKILL.md` must begin with YAML frontmatter containing a unique kebab-case `name` and a concise `description` that states what the skill does and when it applies.

Within **Definitions and calculation logic**, every specialist must load both shared controls before interpreting input:

- `../../docs/supported-files.md`, including its source-trust and document-safety rules
- `../../docs/calculations.md`, for shared formulas and ratio conventions

## Data labels

Every material figure in an output should be treated as one of:

- **Reported**: directly sourced from user-provided data.
- **Calculated**: mathematically derived from reported data.
- **Assumption**: provided by the user or explicitly introduced for scenario analysis.
- **AI interpretation**: analytical explanation or inference based on the above.

Do not blur these categories.

## Materiality

Prefer material insights over exhaustive commentary. If no materiality threshold is provided:
- use 5% for major P&L or balance-sheet line changes as an initial screen
- use 10% for budget-vs-actual variance screening
- override those screens when the absolute value is financially significant

Always state the threshold used.
