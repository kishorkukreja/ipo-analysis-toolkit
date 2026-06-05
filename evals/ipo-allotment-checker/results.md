# IPO Allotment Checker Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-allotment-checker |
| Date | 2026-06-05 |
| Pass rate | 20/20 (100%) |
| Critical failures | 0 |
| Gate | Passed: >=18/20 and no critical failures |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| q01 | Pass | Workflow requires registrar identification, official route first, BSE/NSE fallback, and no PAN request. |
| q02 | Pass | Registrar reference includes KFin official URL and identifier minimization. |
| q03 | Pass | Registrar reference covers MUFG Intime former Link Intime branding and inputs. |
| q04 | Pass | Bigshare inputs are documented with privacy and official-link caveats. |
| q05 | Pass | Troubleshooting reference treats BSE record-not-found as non-final and asks for route/broker checks. |
| q06 | Pass | Registrar priority and NSE fallback role are explicit. |
| q07 | Pass | Timeline reference uses T+3, T+2 unblock, and normal-window guidance. |
| q08 | Pass | Escalation flow covers lien checks, broker/bank/registrar, then SCORES. |
| q09 | Pass | Demat credit timing and DP/registrar escalation are covered. |
| q10 | Pass | Oversubscribed retail lottery logic and no-guarantee caveat are included. |
| q11 | Pass | Technical rejection causes are listed without overclaiming. |
| q12 | Pass | Post-2025-07-01 SME Individual Investor, two-lot minimum, and no cut-off are included. |
| q13 | Pass | Skill says issue open date controls and not to apply post-July rules blindly. |
| q14 | Pass | Missing dropdown fallback covers registrar verification, exact links, BSE/NSE, and BOA. |
| q15 | Pass | SKILL.md and safety reference prohibit requesting or repeating sensitive identifiers. |
| q16 | Pass | Safety reference warns against paid guaranteed allotment and PAN-sharing scams. |
| q17 | Pass | Output template includes unknown fields, missing-data caveats, sources, and fallback request behavior. |
| q18 | Pass | BOA is framed as aggregate confirmation, not individual private status. |
| q19 | Pass | Current T+3 default and T+6 historical handling are explicit. |
| q20 | Pass | Broker bid status, exchange verification, mandate failure, registrar finalization, and no guarantee are covered. |

## Improvements Made

- Split detailed material into registrar, timeline/SME, and troubleshooting/safety references for progressive disclosure.
- Added explicit privacy minimization rules to the main skill and template.
- Corrected inherited stale T+6 planning language by making T+3 the mandatory current default.
- Added SME issue-open-date gating for the July 2025 process changes.
- Added missing-data fallback behavior for unknown registrars, inactive registrar dropdowns, and unavailable live data.

## Files Created

- `skills/ipo-allotment-checker/SKILL.md`
- `skills/ipo-allotment-checker/references/registrar-lookup.md`
- `skills/ipo-allotment-checker/references/timeline-and-sme.md`
- `skills/ipo-allotment-checker/references/troubleshooting-and-safety.md`
- `skills/ipo-allotment-checker/assets/output-template.md`
- `evals/ipo-allotment-checker/questions.jsonl`
- `evals/ipo-allotment-checker/rubric.md`
- `evals/ipo-allotment-checker/results.md`

## Remaining Risks

- Registrar portals and URLs can change or become temporarily inactive; live answers must verify current official sources when needed.
- Some SME issue terms may differ by prospectus or exchange circular; answers must verify issue opening date and official terms before applying process-specific guidance.
- Manual eval was performed against the static skill artifacts; no automated LLM-eval harness exists in this repository.

## Commit

- Commit hash is reported in the final handoff after commit creation.
