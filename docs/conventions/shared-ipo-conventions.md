# Shared IPO Conventions

These conventions are shared by all 12 IPO skills.

## Plugin Boundary

This repository is the final package boundary for IPO skills. The existing `finance-trading-skills` repository is a planning and research source only during this phase.

Per-skill threads must not write to:

- `finance-trading-skills/skills`
- `finance-trading-skills/docs`
- any sibling repo other than `indian-ipo-skills`

## Required Skill Folder Contract

Each skill thread creates:

```text
skills/[skill-name]/
  SKILL.md
  assets/output-template.md
  references/

evals/[skill-name]/
  questions.jsonl
  rubric.md
  results.md
```

The `skills/shared` folder is reserved for foundation-level references only.

## Trigger and Runtime Behavior

- Skill frontmatter must include a clear `name` and a domain-specific `description`.
- If live or current IPO information is needed, the skill must browse or fetch current sources.
- If a supplied DRHP/RHP/prospectus URL exists, use it directly before searching.
- If a required document cannot be found, ask for the exact URL rather than inventing details.

## Output Contract

Every skill output should include:

- IPO name and classification: mainboard or SME.
- Data freshness: date and source checks.
- Source table with primary and fallback sources.
- Findings section.
- Retail investor implications.
- Caveats and missing data.

`ipo-apply-advisor` must end with a verdict block:

```text
## Verdict
| Field | Value |
|---|---|
| Decision | Apply / Avoid / Neutral |
| Confidence | High / Medium / Low |
| Bias adjusted | Yes / No |
| Category | Retail / sHNI / bHNI / Individual Investor |
| Amount needed | INR amount and lot count |
| Cut-off price | Yes / No / Not available |
```

## Correct Current Defaults

- IPO listing timeline default: T+3 working days.
- T is issue closing date.
- T+3 is mandatory for public issues opening on or after 2023-12-01.
- SME IPO process changed for issues opening on or after 2025-07-01.

## Prohibited Assumptions

- Do not assume GMP is reliable, official, or regulated.
- Do not assume a mainboard retail minimum applies to SME IPOs.
- Do not assume cut-off bidding is available for SME IPOs after the new process applies.
- Do not assume subscription data is final unless the source timestamp confirms it.
