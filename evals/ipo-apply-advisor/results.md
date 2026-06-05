# IPO Apply Advisor Eval Results

Evaluation date: 2026-06-05

## Gate

- Questions: 20
- Required pass rate: 18/20 or better
- Critical failures allowed: 0
- Result: 20/20 pass, 0 critical failures

## Method

Manual rubric review of the authored skill, references, and output template against each JSONL prompt. The eval checks whether a competent agent loading `SKILL.md` and relevant references has explicit instructions to satisfy each question and avoid each critical failure.

## Results

| ID | Status | Notes |
|---|---|---|
| q01 | Pass | Reuse of all prior outputs, listing/long-term split, mainboard retail cut-off, and verdict block are explicit. |
| q02 | Pass | Auto-avoid gates force Avoid for cash-conversion failure despite GMP/subscription. |
| q03 | Pass | Expensive valuation, zero GMP, listing-only horizon, and contradiction handling are covered. |
| q04 | Pass | Missing dependent outputs require source lookup, inline fill, or asking for the offer document. |
| q05 | Pass | SME risk, post-July-2025 process, RPT/profit-spike auto-avoid, and liquidity risk are explicit. |
| q06 | Pass | SME issue-date check prevents blind post-July-2025 rule application to a 2025-06-20 issue. |
| q07 | Pass | Bias check against Apply and retail/NII hype vs weak QIB are explicitly required. |
| q08 | Pass | Bias check against Avoid and negative GMP vs strong fundamentals are covered. |
| q09 | Pass | sHNI guidance rejects capital deployment solely for allotment odds and flags payment feasibility. |
| q10 | Pass | Listing-gain-only Apply/Neutral framing with capped GMP and long-term caveats is covered. |
| q11 | Pass | Pure OFS, weak growth, expensive valuation, and GMP override prevention are covered. |
| q12 | Pass | Source hierarchy, timestamp caveat, conflicting GMP including zero-vs-premium conflict, and low confidence rules are covered. |
| q13 | Pass | Verdict block fields and amount/lot/cut-off fields are defined. |
| q14 | Pass | Market maker is described as minimum liquidity support, not a bullish/no-risk signal. |
| q15 | Pass | Current T+3 baseline and T as closing date are explicit. |
| q16 | Pass | Promoter pledge above 75% is an auto-avoid gate that GMP/QIB cannot offset. |
| q17 | Pass | Loss-making/new-age IPOs require unit economics and not forced P/E. |
| q18 | Pass | Anchor lock-in overhang is handled as listing support with hold-period caveat. |
| q19 | Pass | Safety boundary blocks all-in personalized advice and GMP guarantees, especially SME. |
| q20 | Pass | Weighted score cannot mechanically produce Apply when primary RHP parsing failed, official subscription is missing, and a hard-gate risk may apply. |

## Residual Risks

- Manual evals validate instruction coverage, not live-agent output quality on real IPOs.
- Weighted scorecard behavior now depends on agents preserving confidence caps and hard gates when aggregating multiple skill outputs.
- Current IPO facts still require browsing or fresh source checks at runtime.
- SME process details can change; the skill instructs verification against exchange/SEBI sources before user-action guidance.
