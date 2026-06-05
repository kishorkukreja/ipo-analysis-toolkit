# IPO Red Flags Detector Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | ipo-red-flags-detector |
| Date | 2026-06-05 |
| Pass rate | 20/20, 100% |
| Critical failures | 0 |
| Gate | PASS - above 18/20 and no critical failures |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| q01 | Pass | OFS thresholds, growth-capital contradiction, source hierarchy, and GMP caveat are covered. |
| q02 | Pass | Positive PAT with negative OCF in 2 of 3 years maps to auto-reject unless supported sector mechanics exist. |
| q03 | Pass | Pledge > 75% triggers auto-reject; group-debt pledge escalation and bounded language are covered. |
| q04 | Pass | RPT revenue, advances/net worth, and circular customer/supplier risk are covered with denominator caveats. |
| q05 | Pass | Litigation scaled to net worth, SEBI penalty, unquantified criminal case, and data-gap handling are covered. |
| q06 | Pass | Adverse audit opinion and recent auditor change trigger auto-reject/critical handling without defamation. |
| q07 | Pass | Material restatement > 10%, loss-to-profit, and revenue recognition criticality are covered. |
| q08 | Pass | SME, 2025-08-04 open date, post-2025-07-01 verification, promoter-related loan repayment, and GCP cap are covered. |
| q09 | Pass | SME market-maker absence, free-float liquidity, and GMP caveats are covered. |
| q10 | Pass | Missing DRHP/RHP prevents clean certificate; provisional low-confidence scan and document request are required. |
| q11 | Pass | T+3 current default and stale/historical T+6 handling are explicit. |
| q12 | Pass | Pre-2025-07-01 BSE SME issue avoids blind application of later process rules and separates rule vs heuristic. |
| q13 | Pass | Customer concentration > 40%, related-party customer, contract risk, and SME classification requirement are covered. |
| q14 | Pass | Abridged prospectus mismatch, DRHP priority, RPTs, and auditor emphasis are covered. |
| q15 | Pass | SME multiplier, sudden PAT spike, negative OCF, receivables, banker risk, and composite critical rules are covered. |
| q16 | Pass | Clean checks are allowed only with data-gap penalty, confidence limits, and missing-section disclosure. |
| q17 | Pass | GMP/subscription cannot override weak OCF and RPT-backed revenue; no guaranteed listing gains. |
| q18 | Pass | Mainboard GCP/OFS/auditor/OCF thresholds and composite critical scoring are covered. |
| q19 | Pass | Active SEBI fund-diversion order remains auto-reject risk even if disclosed; attribution caveat included. |
| q20 | Pass | Output-template compliance, source caveat, missing information, and safety note are covered. |

## Improvements Made

- Split the skill into a short workflow plus focused references for thresholds, SME rules/liquidity, and evidence/safety.
- Added explicit T+3 timeline handling and July 2025 SME date-gating.
- Added exact 20-question eval coverage across offer structure, accounting quality, governance, SME liquidity, missing data, output compliance, and safety.

## Remaining Risks

- SME framework details can change; final answers must verify current SEBI/NSE/BSE sources before stating a regulatory breach.
- The skill depends on users or browsing tools providing DRHP/RHP data; secondary-source-only scans must remain provisional.

