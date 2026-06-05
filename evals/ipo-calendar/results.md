# IPO Calendar Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-calendar |
| Date | 2026-06-05 |
| Questions | 20 |
| Pass rate | 20/20 (100%) |
| Critical failures | 0 |

## Method

Rubric-based qualitative review of `skills/ipo-calendar/SKILL.md`, `skills/ipo-calendar/references/*.md`, and `skills/ipo-calendar/assets/output-template.md` against `evals/ipo-calendar/questions.jsonl`.

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| q01 | Pass | Default both-market scope, live web requirement, separate mainboard/SME sections, and template sections are explicit. |
| q02 | Pass | Required fields include price band, lot size, registrar, and RHP/prospectus links with official source preference. |
| q03 | Pass | SME platform, lot size, minimum amount, classification, and risk caveats are required. |
| q04 | Pass | Closed statuses and expected T+3 computation rules are covered, with official dates preferred. |
| q05 | Pass | Conflict handling prefers official exchange data and requires naming conflicts. |
| q06 | Pass | Filed-stage status is separate from upcoming and SEBI filing alone cannot be scheduled. |
| q07 | Pass | Recently listed status, listing date, issue price, and classification fields are covered. |
| q08 | Pass | Post-2025-07-01 SME rules require two lots above INR 2 lakh and no cut-off bidding, subject to official verification. |
| q09 | Pass | Pre-2025-07-01 SME issues are explicitly not forced into the new process. |
| q10 | Pass | T+6 is rejected as current default and T+3 is required. |
| q11 | Pass | Secondary-source-only calendars are allowed only with caveats and official-source preference. |
| q12 | Pass | Missing registrar behavior requires "Not found in checked sources" and specific next-source request. |
| q13 | Pass | Subscription snapshots require source and timestamp. |
| q14 | Pass | Apply decision and GMP-only verdicts are blocked and routed to `ipo-apply-advisor`. |
| q15 | Pass | Normal IPO calendar filters out debt, REITs, InvITs, rights, and non-equity issues unless requested. |
| q16 | Pass | Single-company classification lookup and unknown classification behavior are required. |
| q17 | Pass | Output template includes all requested sections. |
| q18 | Pass | Secondary price-band fields must be labeled and official gaps disclosed. |
| q19 | Pass | Official dates override computed T+3 dates; conflicts are noted. |
| q20 | Pass | Default India-only, both-market scope and concise template-compatible response are supported. |

## Improvements Made

- Added explicit source hierarchy with official SEBI/NSE/BSE/registrar priority and secondary-source caveats.
- Added normalized calendar statuses to avoid treating filed-stage companies as scheduled IPOs.
- Added T+3 timeline handling with computed-date labeling and T+6 stale-source correction.
- Added SME process branching for issues opening before, on, and after 2025-07-01.
- Added a locked output template with freshness, source priority, mainboard, SME, T+3 timeline, missing data, caveats, and next actions.
- Added safety boundary against apply/avoid decisions, guaranteed returns, guaranteed allotment, and GMP-only conclusions.

## Failed Cases

None.

## Files Created

- `skills/ipo-calendar/SKILL.md`
- `skills/ipo-calendar/references/source-hierarchy.md`
- `skills/ipo-calendar/references/calendar-fields.md`
- `skills/ipo-calendar/references/timeline-and-sme-rules.md`
- `skills/ipo-calendar/assets/output-template.md`
- `evals/ipo-calendar/questions.jsonl`
- `evals/ipo-calendar/rubric.md`
- `evals/ipo-calendar/results.md`

## Remaining Risks

- NSE and BSE pages can be dynamic or intermittently unavailable, so agents may need search snippets, CSV downloads, or secondary-source cross-checks.
- SME process details may vary by exchange circular, offer document, category, broker interface, and final-day timing; the skill requires verification before application guidance.
- Aggregator data can lag official updates, especially date changes, registrar links, listing dates, and issue extensions.
- This qualitative eval checks instructions and expected behavior, not a live run against a specific real-time IPO calendar.
