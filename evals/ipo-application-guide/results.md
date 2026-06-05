# IPO Application Guide Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-application-guide |
| Date | 2026-06-05 |
| Eval method | Manual/static rubric evaluation of `SKILL.md`, references, and output template against 20 JSONL scenarios |
| Questions | 20 |
| Passed | 20 |
| Failed | 0 |
| Pass rate | 100% |
| Critical failures | 0 |
| Gate | PASS: >=18/20 and no critical failures |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| ipo-application-guide-001 | Pass | Broker UPI ASBA workflow, mandate approval, own UPI ID, ASBA block, and privacy covered. |
| ipo-application-guide-002 | Pass | No-mandate troubleshooting covers routing lag, deadline checks, incomplete application caveat, and bank ASBA fallback. |
| ipo-application-guide-003 | Pass | Distinguishes INR 5 lakh UPI mandate limit from INR 2 lakh mainboard retail cap and category shift to NII. |
| ipo-application-guide-004 | Pass | Cut-off meaning, cap-price block, mainboard retail eligibility, and below-final-price risk covered. |
| ipo-application-guide-005 | Pass | NII/HNI no cut-off, no withdrawal/lower bid, upward revision caveat, and bank ASBA preference covered. |
| ipo-application-guide-006 | Pass | Bank ASBA workflow, SCSB/netbanking route, demat/PAN fields, lien check, and rejection risks covered. |
| ipo-application-guide-007 | Pass | Revised SME process for 2025-07-10 covered: 2 lots above INR 2 lakh, no cut-off, no cancellation/reduction, 4 PM/5 PM deadlines. |
| ipo-application-guide-008 | Pass | Pre-July 2025 SME issue handled with date verification and no blind application of revised process. |
| ipo-application-guide-009 | Pass | Amount formula, cap price for cut-off, lot multiples, retail cap, and sample INR 15,000 one-lot calculation covered. |
| ipo-application-guide-010 | Pass | One valid application per PAN/category, duplicate same-PAN risk, and no loophole advice covered. |
| ipo-application-guide-011 | Pass | Current T+3 working-day timeline covered with T+1/T+2/T+3 milestones and holiday caveat. |
| ipo-application-guide-012 | Pass | Registrar-first workflow, common registrars, BSE/NSE alternatives, official pages, and privacy covered. |
| ipo-application-guide-013 | Pass | ASBA unblock vs refund distinction, bank lien as authoritative status, and escalation path covered. |
| ipo-application-guide-014 | Pass | Mandate-approved/broker-pending sync lag, bank block check, application reference, and duplicate-caution covered. |
| ipo-application-guide-015 | Pass | Demat credit timing, active demat, DP/client ID, registrar/DP escalation, and schedule caveat covered. |
| ipo-application-guide-016 | Pass | Required details before cancellation/reduction advice and category-specific rules covered. |
| ipo-application-guide-017 | Pass | Missing issue data fallback asks for official details and avoids fabrication. |
| ipo-application-guide-018 | Pass | Common rejection and operational failure list covers mandate, UPI, mismatch, balance, lot/price, and deadline errors. |
| ipo-application-guide-019 | Pass | Output template includes scope, facts, interpretation, action, timeline, troubleshooting, and safety sections. |
| ipo-application-guide-020 | Pass | Rejects guaranteed allotment/listing gains and redirects to safe process guidance. |

## Improvements Made During Evaluation

- Added explicit shared-reference cross-links to `skills/shared/references/india_ipo_data_sources.md`, `skills/shared/references/sme_vs_mainboard.md`, and `skills/shared/references/registrars.md`.
- Kept T+3 as current default and marked T+6 as historical or issue-specific only.
- Added critical checks for UPI mandate completion, third-party UPI/bank rejection risk, duplicate PAN applications, SME July 2025 process, and no guarantee claims.

## Files Created

- `skills/ipo-application-guide/SKILL.md`
- `skills/ipo-application-guide/references/application-rules.md`
- `skills/ipo-application-guide/references/workflows-and-troubleshooting.md`
- `skills/ipo-application-guide/references/sources-and-privacy.md`
- `skills/ipo-application-guide/assets/output-template.md`
- `evals/ipo-application-guide/questions.jsonl`
- `evals/ipo-application-guide/rubric.md`
- `evals/ipo-application-guide/results.md`

## Remaining Risks

- Broker and bank UI labels, cutoffs, and supported categories can change; users must verify the live issue page and platform notices.
- SME process guidance depends on issue open date; pre-2025-07-01 and spillover cases need official exchange or offer-document confirmation.
- Registrar pages may activate only after basis of allotment finalization, so status availability can lag the schedule.
