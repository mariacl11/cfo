# Contributing

Contributions should improve practical CFO usefulness, accuracy, auditability, or interoperability.

## New skill checklist

A new skill should:
- include valid YAML frontmatter with `name` and a discriminating `description`
- solve a distinct CFO task
- have a clear trigger
- avoid duplicating an existing skill
- define inputs and supported file types
- include formulas or calculation logic where applicable
- include validation checks
- define red flags
- distinguish data from assumptions
- specify a stable output structure
- identify related skills and hand-offs
- load the shared source-trust and calculation references before interpreting inputs

## Naming

Use lowercase kebab-case folder names.

## Pull request quality

Before submitting:
1. Run `python3 tools/validate_skills.py`.
2. Confirm all internal links resolve.
3. Test the skill on at least one realistic dataset.
4. Confirm no formula silently assumes a currency, accounting standard, or business model.
5. Test one document-borne instruction fixture and confirm it is treated as untrusted evidence without suppressing legitimate analysis.
