# Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-financials-scorer |
| Date | 2026-06-05 |
| Pass rate | 20/20 (100%) |
| Critical failures | 0 |
| Gate | Passed: >=18/20 and no critical failures |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| q01 | Pass | Happy path covered by SKILL workflow, scoring model, formulas, and template sections. |
| q02 | Pass | Missing data behavior requires full offer document lookup, limited fallback, reduced confidence, and no invented ratios. |
| q03 | Pass | DRHP extraction fallback explicitly treats abridged prospectus as navigation or limited fallback with cross-check caveat. |
| q04 | Pass | SME classification, issue open date, stricter SME caps, negative CFO, and 45% top-customer cap are covered. |
| q05 | Pass | Current T+3 default is explicit; T+6 is historical only. |
| q06 | Pass | Receivable-led growth and weak CFO/PAT trigger growth-quality and working-capital penalties. |
| q07 | Pass | Pre/post debt repayment handling and critical interest-cover override are included. |
| q08 | Pass | SaaS and loss-making rules prevent PAT CAGR/P/E misuse and require runway/unit economics. |
| q09 | Pass | Bank/NBFC substitution avoids generic D/E, EBITDA, ROCE, and working-capital scoring. |
| q10 | Pass | Output requires issuer-reported versus skill-computed metrics and formula differences. |
| q11 | Pass | EPC sector model covers order book, retention money, negative CFO, and cap logic. |
| q12 | Pass | Retail/QSR model allows low PAT margin when cash cycle and store metrics are strong. |
| q13 | Pass | Auditor qualification is a critical override, so raw 78 cannot remain Strong. |
| q14 | Pass | SME, merger normalization, and fewer-than-three-years cap are covered. |
| q15 | Pass | Payables-driven CFO is caveated and affects cash conversion/working-capital score. |
| q16 | Pass | Safety boundary blocks apply/avoid advice and guaranteed listing gains. |
| q17 | Pass | Brokerage review is allowed only as labeled fallback with low confidence and refresh caveat. |
| q18 | Pass | Objects of issue, working-capital funding, and weak CFO cap are covered. |
| q19 | Pass | Stub periods stay separate; balance-sheet working capital is not annualized. |
| q20 | Pass | Template includes source checks, breakdown, key financials, ratios, normalizations, overrides, implications, and handoff fields. |

## Improvements Made

- Added explicit fallback rules for PDF extraction failure, abridged prospectus use, and secondary-source-only scoring.
- Added direct safety language blocking apply/avoid/subscribe verdicts and guaranteed outcomes.
- Added current T+3 timeline language and SME issue-date handling.
- Split formulas, scoring thresholds, sector adjustments, and overrides into references for progressive disclosure.
- Added template fields for issuer-reported versus skill-computed KPIs, source caveats, confidence, SME adjustments, and handoff fields.

## Remaining Risks

- The eval is rubric-based and artifact-level; it does not run live PDF extraction against a real DRHP.
- Thresholds are heuristic and should be refreshed if SEBI or exchange disclosure requirements materially change.
- Sector-specific models may need further calibration after testing on real IPOs across banks/NBFCs, SaaS, EPC, retail, and manufacturing.
