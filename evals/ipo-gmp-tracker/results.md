# IPO GMP Tracker Eval Results

## Run 1 - 2026-06-05

Model/tooling: Manual static evaluation of created skill instructions, references, output template, and 20-question JSONL dataset.

Questions run: 20

Pass summary: 20/20 passed

Critical failures: 0

## Question Results

| ID | Result | Notes |
|---|---|---|
| ipo-gmp-tracker-001 | Pass | SKILL requires live verification, multiple GMP sources, timestamps, GMP math, and caveats. |
| ipo-gmp-tracker-002 | Pass | Methodology reference includes formula and exact positive GMP example. |
| ipo-gmp-tracker-003 | Pass | Methodology reference handles negative GMP and per-lot loss. |
| ipo-gmp-tracker-004 | Pass | Source agreement thresholds and reliability scoring are defined. |
| ipo-gmp-tracker-005 | Pass | Disagreement handling requires range display and reliability caps. |
| ipo-gmp-tracker-006 | Pass | One-source/no-timestamp hard caps are explicit. |
| ipo-gmp-tracker-007 | Pass | SME one-source cap, lot-size math, and SME liquidity caveats are required. |
| ipo-gmp-tracker-008 | Pass | SME interpretation is explicitly more conservative than mainboard. |
| ipo-gmp-tracker-009 | Pass | Trend reference classifies falling-from-high and hype fading. |
| ipo-gmp-tracker-010 | Pass | Reliability framework caps high GMP with weak QIB near close. |
| ipo-gmp-tracker-011 | Pass | Trend reference flags round-number stickiness. |
| ipo-gmp-tracker-012 | Pass | Skill and methodology prohibit listing math from Kostak/STS. |
| ipo-gmp-tracker-013 | Pass | Skill prohibits GMP-only apply/avoid recommendations. |
| ipo-gmp-tracker-014 | Pass | Skill and rubric require unofficial/unregulated caveat. |
| ipo-gmp-tracker-015 | Pass | Skill uses T+3 working days and defines T as close date. |
| ipo-gmp-tracker-016 | Pass | Skill treats T+6 as historical except for older issue-specific documents. |
| ipo-gmp-tracker-017 | Pass | Skill requires SME issue open date and July 2025 process caution. |
| ipo-gmp-tracker-018 | Pass | Missing-data behavior says not to compute or invent GMP. |
| ipo-gmp-tracker-019 | Pass | Output template includes required sections. |
| ipo-gmp-tracker-020 | Pass | Promotional/manipulation red flags cap reliability at Low. |

## Files Created

- `skills/ipo-gmp-tracker/SKILL.md`
- `skills/ipo-gmp-tracker/references/gmp-methodology.md`
- `skills/ipo-gmp-tracker/references/source-and-reliability.md`
- `skills/ipo-gmp-tracker/references/trend-interpretation.md`
- `skills/ipo-gmp-tracker/assets/output-template.md`
- `evals/ipo-gmp-tracker/questions.jsonl`
- `evals/ipo-gmp-tracker/rubric.md`
- `evals/ipo-gmp-tracker/results.md`

## Remaining Risks

- Current GMP answers depend on live web access and publisher availability.
- Some GMP sites may expose timestamps inconsistently, so the skill must label freshness as unknown when needed.
- Conflicting GMP sources must be shown as a range with a confidence cap, not collapsed into one precise implied listing price.
- SME process details after 2025-07-01 should still be verified from exchange or SEBI sources when they affect user action.
