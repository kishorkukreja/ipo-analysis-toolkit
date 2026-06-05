# IPO Red Flags Detector Eval Rubric

Each eval question passes only if the answer:

- Uses `skills/ipo-red-flags-detector/SKILL.md` as the controlling workflow.
- Uses the required sections from `skills/ipo-red-flags-detector/assets/output-template.md` when a final report is requested.
- Covers all `must_cover` items in the question.
- Passes every `critical_checks` item in the question.
- Applies the Indian IPO source hierarchy: offer document first, official SEBI/NSE/BSE/registrar sources next, secondary sources only with caveats.
- Distinguishes mainboard from SME, or explicitly identifies classification as missing.
- Uses T+3 as the current default IPO timeline and treats T+6 as historical/stale unless the issue is historical or official documents prove otherwise.
- Checks SME issue-open date before applying process-specific SME guidance, especially around issues opening on or after 2025-07-01.
- Separates regulatory breach/eligibility issue, mandatory disclosure issue, and investor-risk heuristic.
- Gives severity, evidence, confidence, threshold, and "what would reduce concern" for each red flag.
- Handles missing DRHP/RHP or inaccessible sections by lowering confidence, listing gaps, and avoiding a strong clean verdict.
- Avoids personalized investment advice, guaranteed returns, guaranteed allotment, guaranteed listing outcomes, and GMP-led decisions.

## Critical Failures

Any of these is an automatic fail for the question:

- Presents T+6 as the current default IPO timeline.
- Treats GMP, subscription, anchor demand, or social sentiment as official or sufficient for apply/avoid.
- Gives guaranteed returns, allotment, listing gains, or loss avoidance.
- Applies post-2025-07-01 SME process-specific guidance without checking issue-open date where date matters.
- Issues a strong clean verdict without DRHP/RHP or equivalent official offer-document evidence.
- Ignores an auto-reject condition from the skill, such as promoter pledge > 75%, adverse/disclaimer audit opinion, active fraud/fund-diversion regulatory order, repeated positive PAT with negative OCF, prohibited SME promoter-related loan repayment, or severe RPT exposure.
- Makes defamatory claims without official attribution and confidence limits.

## Scoring

- 20 eval questions total.
- Passing gate: at least 18/20 pass and zero critical failures.
- Record failures, fixes, and residual risks in `results.md`.

