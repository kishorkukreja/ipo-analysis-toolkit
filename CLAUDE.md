# Indian IPO Plugin Conventions

Use these conventions for every skill in this repository.

## Boundary

- This is a separate installable IPO plugin.
- Do not create or modify IPO skills in `finance-trading-skills/skills`.
- Shared references live in `skills/shared/references`.
- Skill-specific references live in `skills/[skill-name]/references`.
- Skill output templates live in `skills/[skill-name]/assets/output-template.md`.

## Market Scope

- India only.
- Cover NSE/BSE mainboard IPOs and SME IPOs on NSE Emerge and BSE SME.
- State whether the issue is mainboard or SME before giving application, allotment, or risk guidance.

## Formatting

- Use INR amounts in words or `INR` notation in markdown text.
- Use Indian fiscal years as Apr-Mar.
- State dates in `YYYY-MM-DD` when the date affects regulatory treatment or timelines.
- Use structured markdown tables for scorecards, verdicts, timelines, and source checks.
- Always separate facts, interpretation, and retail investor action.

## Timeline Defaults

- Default IPO listing timeline is T+3 working days, where T is issue closing date.
- T+3 became mandatory for public issues opening on or after 2023-12-01.
- Do not use T+6 as the current default. Mention T+6 only as historical context or if an older offer document explicitly applies it.

## SME IPO Rules

For SME IPOs, branch guidance by issue opening date:

- Issues opening before 2025-07-01 may use the old SME bidding process, subject to exchange-specific transition handling.
- Issues opening on or after 2025-07-01 use the new SME bidding process.
- Under the new process, skills must check minimum application size, lot requirements, cut-off bidding availability, bid revision/cancellation rules, and final-day timing before advising the user.

## Data Source Discipline

- Web-verify live data such as GMP, subscription, calendar status, allotment links, and registrar pages.
- Prefer primary sources for regulations and official documents: SEBI, NSE, BSE, registrar websites, and offer documents.
- Use secondary IPO data sources only when official sources are inaccessible or for cross-checking.
- GMP is informal and unregulated. Never present GMP as guaranteed listing gain.

## Retail Investor Framing

- This plugin is for retail investor decision support, not personalized investment advice.
- Explain risk in plain language.
- For `ipo-apply-advisor`, include an explicit confidence level and state missing or stale inputs.
