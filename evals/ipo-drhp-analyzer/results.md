# ipo-drhp-analyzer Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-drhp-analyzer |
| Date | 2026-06-05 |
| Evaluator | Manual rubric review by Codex thread |
| Questions run | 20 |
| Passed | 20 |
| Failed | 0 |
| Pass rate | 100% |
| Critical failures | 0 |
| Gate | Passed: at least 18/20 and no critical source, safety, or regulatory-timeline failures |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| ipo-drhp-analyzer-001 | Pass | Provided official URL is used first; template and official-source priority are explicit. |
| ipo-drhp-analyzer-002 | Pass | Skill requires SEBI/NSE/BSE/SME exchange search and asks for URL if not found. |
| ipo-drhp-analyzer-003 | Pass | PDF fallback flow downgrades confidence and keeps missing fields explicit. |
| ipo-drhp-analyzer-004 | Pass | SME classification and post-2025-07-01 checks are required. |
| ipo-drhp-analyzer-005 | Pass | Transition issue requires issue open date and avoids blindly applying post-July rules. |
| ipo-drhp-analyzer-006 | Pass | 100% OFS flag states company receives no growth capital. |
| ipo-drhp-analyzer-007 | Pass | Objects section applies only to fresh issue proceeds. |
| ipo-drhp-analyzer-008 | Pass | Risk extraction keeps issuer summary plus retail meaning and categories. |
| ipo-drhp-analyzer-009 | Pass | Litigation table requires party, forum, amount, status, and retail meaning. |
| ipo-drhp-analyzer-010 | Pass | Promoter section links OFS, RPT, and litigation context. |
| ipo-drhp-analyzer-011 | Pass | RHP limitations prevent invented final price. |
| ipo-drhp-analyzer-012 | Pass | Completed IPO workflow prefers prospectus and requires DRHP/RHP for change analysis. |
| ipo-drhp-analyzer-013 | Pass | T+3 is current default; T+6 is historical/source-specific only. |
| ipo-drhp-analyzer-014 | Pass | T is issue closing date and T+3 working days is mandatory after 2023-12-01. |
| ipo-drhp-analyzer-015 | Pass | SME cut-off guidance is date-gated and scoped away from direct application advice. |
| ipo-drhp-analyzer-016 | Pass | Secondary-only source produces Low confidence and asks for official URL. |
| ipo-drhp-analyzer-017 | Pass | Scanned/broken tables require OCR/manual review and confidence downgrade. |
| ipo-drhp-analyzer-018 | Pass | Basis-for-price section is extraction, not a final valuation or apply verdict. |
| ipo-drhp-analyzer-019 | Pass | Template contains required header, source checks, offer structure, objects, risks, litigation, financial snapshot, caveats, and takeaways. |
| ipo-drhp-analyzer-020 | Pass | GMP is treated as informal and not a guarantee; skill stays in document-risk scope. |

## Improvements Made During Review

- Added official RHP/PDF retrieval failure fallback chain: SEBI page, issuer PDF, exchange page, abridged prospectus, BRLM/registrar, then labeled secondary sources.
- Tightened `SKILL.md` to state T+3 as current default and T+6 as historical unless issue-specific evidence applies.
- Added SME issue-open-date branch and post-2025-07-01 checks to prevent stale SME mechanics.
- Added explicit source confidence labels and secondary-source restrictions.
- Added OFS thresholds and the rule that OFS proceeds generally do not fund issuer objects.
- Added PDF parsing caveats for scanned/table-heavy offer documents.
- Expanded the output template to force source checks, missing data, SME-specific checks, and retail caveats.

## Failed Cases

None.

## Files Created

- `skills/ipo-drhp-analyzer/SKILL.md`
- `skills/ipo-drhp-analyzer/references/source-and-fallbacks.md`
- `skills/ipo-drhp-analyzer/references/drhp-section-map.md`
- `skills/ipo-drhp-analyzer/references/retail-interpretation.md`
- `skills/ipo-drhp-analyzer/assets/output-template.md`
- `evals/ipo-drhp-analyzer/questions.jsonl`
- `evals/ipo-drhp-analyzer/rubric.md`
- `evals/ipo-drhp-analyzer/results.md`

## Remaining Risks

- Live official URLs and circular names may move; the skill requires current source lookup before live IPO analysis.
- PDF extraction quality depends on the runtime tools available for long scanned offer documents.
- SME process interpretation should be rechecked against the latest SEBI/exchange circulars when an issue opens after any future rule change.
