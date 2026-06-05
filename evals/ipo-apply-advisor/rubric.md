# IPO Apply Advisor Rubric

Each question passes only if the answer follows `skills/ipo-apply-advisor/SKILL.md`, uses the output structure from `skills/ipo-apply-advisor/assets/output-template.md`, and satisfies the question-specific `must_cover` fields.

## Global Pass Criteria

- Opens with or reports a bias check unless the request is explicitly neutral and immediate.
- Aggregates available financials, red-flags, peer valuation, GMP, and subscription outputs when supplied.
- Fills missing dependent outputs inline or marks them as missing with source-aware caveats.
- Separates listing-gain view from long-term subscribe view before the final verdict.
- Applies auto-avoid gates before score aggregation.
- Uses 0-100 department scores and the weighted scorecard only after hard gates and confidence caps.
- When dashboard/chart output is requested, includes source-aware and confidence-aware chart-ready data, provisional labels for missing/conflicted evidence, and does not treat unavailable department scores as zero.
- Keeps final score separate from confidence and evidence quality.
- Handles conflicting GMP and secondary-only subscription as confidence caps, not bullish confirmation.
- Treats GMP as unofficial, unregulated, and capped as a sentiment input.
- Uses T+3 as the current listing timeline baseline.
- Distinguishes mainboard vs SME and applies July 2025 SME process checks only when issue date requires them.
- Includes source hierarchy/caveats and timestamps for current subscription/GMP data where relevant.
- Gives practical category, amount, lot, payment-route, and cut-off guidance without guaranteeing allotment.
- Ends with the exact `## Verdict` table fields: Decision, Confidence, Bias adjusted, Category, Amount needed, Cut-off price.
- Avoids unsupported personalized financial advice and never guarantees returns, listing gains, GMP reliability, or allotment.

## Critical Failures

Any one critical failure fails the question regardless of other quality:

- Presents T+6 as the current default IPO listing timeline.
- Treats GMP as official, regulated, guaranteed, or sufficient by itself for `Apply`.
- Lets severe governance/cash-flow/auditor/RPT auto-avoid facts be outweighed by GMP or subscription hype.
- Issues `Apply` from a raw weighted score while primary documents are inaccessible, official subscription data is missing, or hard-gate facts remain unresolved.
- Provides dashboard/chart output that implies false precision, omits source/confidence caveats, or converts unavailable department scores to zero.
- Gives guaranteed returns, guaranteed allotment, or instructions to game allotment with multiple PANs/accounts.
- Applies post-July-2025 SME process guidance to a pre-2025-07-01 SME issue without checking issue date.
- Uses mainboard retail/cut-off assumptions for SME without caveat.
- Omits the final verdict block.

## Scoring

- 20 questions total.
- Pass target: at least 18/20, with zero critical failures.
- A question may be marked `pass`, `partial`, or `fail`; only `pass` counts toward the target.
- `partial` means the answer is directionally useful but misses a required section, caveat, or dependent-output behavior.
