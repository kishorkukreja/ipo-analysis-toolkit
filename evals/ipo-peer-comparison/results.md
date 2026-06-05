# IPO Peer Comparison Eval Results

## Final Score

| Field | Result |
|---|---:|
| Questions | 20 |
| Passed | 20 |
| Failed | 0 |
| Pass rate | 100% |
| Critical safety failures | 0 |
| Critical source-reliability failures | 0 |
| Critical valuation failures | 0 |
| Critical timeline failures | 0 |

Gate status: Passed. The skill exceeds the required 18/20 threshold and has no critical failures.

## Evaluation Method

Manual rubric evaluation against `evals/ipo-peer-comparison/rubric.md`, using the final contents of:

- `skills/ipo-peer-comparison/SKILL.md`
- `skills/ipo-peer-comparison/assets/output-template.md`
- `skills/ipo-peer-comparison/references/source-and-peer-selection.md`
- `skills/ipo-peer-comparison/references/valuation-methodology.md`
- `skills/ipo-peer-comparison/references/sme-and-special-cases.md`

## Iteration Notes

The final pass checked for the common failure modes from the project contract:

- T+3 is the only current default listing timeline used.
- SME outputs require classification, liquidity caveats, and issue-open-date checks where July 2025 process guidance matters.
- GMP and subscription are explicitly rejected as valuation proof.
- P/E is rejected for negative EPS and for sectors where it is not the primary metric.
- EV/EBITDA is rejected for negative EBITDA unless clearly marked not meaningful.
- Missing peer data lowers confidence instead of producing invented medians.
- Output compliance is locked through `assets/output-template.md`.

## Per-Question Result

| ID | Result | Notes |
|---|---|---|
| q01 | Pass | Covers mainboard profitable P/E, median comparison, and template sections. |
| q02 | Pass | Requires EV/EBITDA where leverage differs and audits DRHP P/E-only framing. |
| q03 | Pass | Rejects fake P/E for loss-making SaaS and requires KPI/global-comp caveats. |
| q04 | Pass | Uses P/B and lender-quality metrics instead of generic P/E. |
| q05 | Pass | Requires P/Embedded Value and insurance KPIs, rejecting P/E primary. |
| q06 | Pass | Covers AMC EV/AUM, AUM mix, flows, and source logging. |
| q07 | Pass | Applies SME liquidity caveat, weak peer count, and stricter premium bands. |
| q08 | Pass | Covers issue-open-date verification, July 2025 SME awareness, and T+3. |
| q09 | Pass | Covers IPO-name-only source workflow and asks for URL if sources fail. |
| q10 | Pass | Requires supplied RHP/DRHP link first and current peer data lookup only as needed. |
| q11 | Pass | Missing peer data lowers confidence; no invented median. |
| q12 | Pass | Global comps are fallback only with low-confidence and adjustment caveats. |
| q13 | Pass | Detects cherry-picked peer table and average/outlier distortion. |
| q14 | Pass | Premium formula gives `(38 / 30) - 1 = 26.7%`. |
| q15 | Pass | Negative EBITDA makes EV/EBITDA not meaningful and shifts to sales/KPIs. |
| q16 | Pass | OFS-heavy premium with in-line growth is treated cautiously without personalized certainty. |
| q17 | Pass | Cyclical peak earnings require mid-cycle context and avoid cheapness claims. |
| q18 | Pass | GMP/subscription are rejected as valuation proof. |
| q19 | Pass | Output sections match the template. |
| q20 | Pass | Safety boundary rejects guaranteed calls and frames research support. |

## Files Created

- `skills/ipo-peer-comparison/SKILL.md`
- `skills/ipo-peer-comparison/references/source-and-peer-selection.md`
- `skills/ipo-peer-comparison/references/valuation-methodology.md`
- `skills/ipo-peer-comparison/references/sme-and-special-cases.md`
- `skills/ipo-peer-comparison/assets/output-template.md`
- `evals/ipo-peer-comparison/questions.jsonl`
- `evals/ipo-peer-comparison/rubric.md`
- `evals/ipo-peer-comparison/results.md`

## Remaining Risks

- The eval is rubric/manual rather than backed by an automated model-grading runner.
- Live peer-price freshness depends on the runtime agent browsing or market-data access.
- Some sector-specific edge cases may still need future examples once sibling IPO skills are integrated.
