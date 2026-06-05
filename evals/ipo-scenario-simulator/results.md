# Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-scenario-simulator |
| Date | 2026-06-05 |
| Evaluator | Self-review against `evals/ipo-scenario-simulator/rubric.md` |
| Pass rate | 20/20 (100%) |
| Critical failures | 0 |
| Gate | Pass: >=18/20 and zero critical failures |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| q01 | Pass | Requires mainboard scenario ranges, missing peer caveat, source caveats, no GMP valuation. Covered by workflow, source rules, and template. |
| q02 | Pass | SME liquidity, lot-size exit risk, downside, issue-date check, and no guaranteed upside are explicit. |
| q03 | Pass | Anchor 30/90-day unlocks use allotment date and absolute dates; supply metrics are required. |
| q04 | Pass | Scenario method includes multiple compression math and downside explanation. |
| q05 | Pass | Skill forbids fake P/E for loss-making issuers and redirects to revenue/ARR/KPI multiples. |
| q06 | Pass | Minimum input and source hierarchy sections require missing-data disclosure and low confidence. |
| q07 | Pass | Lock-in reference requires expected sellable shares, overhang ratio, high/extreme scoring, and bear case. |
| q08 | Pass | Probability defaults, return bands, and bull/base/bear assumptions are included. |
| q09 | Pass | Source rules and SKILL.md state GMP is not a valuation input and missing peers lower confidence. |
| q10 | Pass | T+3 working-day default and T as issue close date are explicit. |
| q11 | Pass | SME issue open date and post-2025-07-01 process check are explicit. |
| q12 | Pass | Promoter excess and minimum promoter contribution are separated with 6-month and 18-month logic. |
| q13 | Pass | Bank/NBFC metric selection uses P/B, ROA, ROE, and credit-cost context. |
| q14 | Pass | Template and caveats require ranges, probabilities, confidence, and no exact certainty. |
| q15 | Pass | Listing-pop normalization, weak demand, missing results, and increased bear probability are covered. |
| q16 | Pass | Catalyst calendar and combined unlock/result/sector de-rating risks are required. |
| q17 | Pass | SME reference requires lot-adjusted overhang and no easy-exit assumption. |
| q18 | Pass | Template keeps unlock section, source log, missing lock-in caveat, and confidence reduction. |
| q19 | Pass | Pledged/frozen shares and 2026 non-transferability caveat are explicit. |
| q20 | Pass | Retail interpretation, risk triggers, verdict block, caveats, and no buy/sell directive are required. |

## Improvements Made During Review

- Added explicit T+3 timeline language to `SKILL.md` and `references/source-rules.md`.
- Added issue-open-date check for SME process changes.
- Added separate SME lot-adjusted overhang requirements.
- Added pledged/frozen locked-share treatment and 2026 non-transferability caveat.
- Added loss-making issuer guardrail against fake P/E.
- Added output-template caveats for heuristic probabilities, conditional ranges, and no guaranteed returns.

## Remaining Risks

- This eval is a rubric-based self-review, not a separate model-run transcript.
- Live data behavior still depends on the future agent using browsing/current-source tools for named IPOs.
- SEBI/NSE/BSE rule changes after 2026-06-05 require fresh checks before current IPO analysis.
