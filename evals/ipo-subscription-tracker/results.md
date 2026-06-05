# IPO Subscription Tracker Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-subscription-tracker |
| Date | 2026-06-05 |
| Questions | 20 |
| Pass rate | 20/20 (100%) |
| Critical failures | 0 |
| Gate | Passed: >=18/20 with no critical source, safety, or timeline failures |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| q01 | Pass | SKILL.md and template require official sources, category-wise table, day-wise trend, anchor book, retail odds, and T+3 note. |
| q02 | Pass | Live/intraday and no-guarantee behavior is explicit in workflow, template, and rubric. |
| q03 | Pass | Category normalization table covers all requested labels and reserved bucket separation. |
| q04 | Pass | Day-wise methodology explains early retail, quiet QIB/NII, and preliminary status. |
| q05 | Pass | Final-day interpretation covers timestamping, QIB quality, NII leverage, and near-close caution. |
| q06 | Pass | Anchor score components and bands support the scoring case. |
| q07 | Pass | Anchor red flags cover concentration, no domestic MF participation, and obscure entities. |
| q08 | Pass | Retail exact probability formula is included with no-guarantee caveat. |
| q09 | Pass | Subscription-multiple proxy is included with method label and limitations. |
| q10 | Pass | Mainboard cutoff guidance distinguishes validity from lottery odds. |
| q11 | Pass | Fixed-price and unavailable cutoff cases are explicitly blocked. |
| q12 | Pass | SME handling requires classification, lot value, liquidity, market maker, and adjusted interpretation. |
| q13 | Pass | Post-2025-07-01 SME process requires official verification before cutoff/revision/cancellation advice. |
| q14 | Pass | Pre-2025-07-01 SME branch avoids automatic new-process assumption. |
| q15 | Pass | Source reconciliation prefers newest official timestamp and labels aggregator caveats. |
| q16 | Pass | Missing-data behavior forbids invention and asks for exact source URLs/documents. |
| q17 | Pass | Current T+3 default and T+6 historical treatment are explicit. |
| q18 | Pass | Output template includes all required sections and missing-data handling. |
| q19 | Pass | GMP separation, no guaranteed gains, and apply-advisor boundary are explicit. |
| q20 | Pass | HNI leverage caveats, funding-cost formula, and no sure-profit rule are explicit. |

## Improvements Made

- Added explicit source hierarchy and reconciliation behavior for conflicting NSE/BSE/aggregator data.
- Added IPO-stage labels and Day 1/opening-day caveats so early retail/NII demand is not over-weighted before final-day QIB behavior is visible.
- Added official-data-missing confidence caps for secondary-only subscription data.
- Added exact and proxy retail allotment formulas with method labeling.
- Added anchor quality score, anchor red flags, and lock-in note.
- Added SME-specific interpretation and July 2025 process verification rules.
- Added cutoff vs price bidding guidance with fixed-price and SME safeguards.
- Added T+3 timeline rule and blocked stale T+6 default usage.
- Added output template sections required by the shared plugin contract.

## Remaining Risks

- The skill depends on live NSE/BSE pages that may be dynamic or temporarily inaccessible, so answers must browse or request exact URLs for current issues.
- July 2025 SME process details should be verified against official issue/platform documents at runtime before giving application mechanics.
- Retail allotment odds remain estimates unless final valid application count or basis-of-allotment data is available.
