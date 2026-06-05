# IPO Scorecard Model

Use this model when a skill produces a department score or when `ipo-apply-advisor` aggregates multiple IPO skill outputs.

## Department Scores

Each department score is reported on a 0-100 scale, separate from confidence.

| Department | Owning skill | Final weight |
|---|---|---:|
| Financial quality | `ipo-financials-scorer` | 25 |
| Valuation / peer comparison | `ipo-peer-comparison` | 20 |
| Governance, red flags, and issue structure | `ipo-red-flags-detector` plus DRHP context | 20 |
| Demand quality | `ipo-subscription-tracker` plus anchor review | 15 |
| GMP / listing sentiment / market mood | `ipo-gmp-tracker` | 10 |
| Application fit, liquidity, timeline, and execution risk | `ipo-application-guide`, `ipo-allotment-checker`, `ipo-listing-day-strategy` | 10 |

## Weighted Final Score

```text
weighted_score =
  financial_quality_score * 0.25 +
  valuation_score * 0.20 +
  governance_issue_structure_score * 0.20 +
  demand_quality_score * 0.15 +
  gmp_listing_sentiment_score * 0.10 +
  application_liquidity_timeline_score * 0.10
```

Do not average missing departments as zero. If a department is unavailable, either fill it from primary sources or mark the final score as provisional and cap confidence at Low or Medium.

## Verdict Bands

| Final score | Base verdict |
|---:|---|
| 75-100 | Apply zone, only if no hard gate exists |
| 55-74 | Neutral zone or wait-for-listing zone |
| 0-54 | Avoid zone |

## Hard Gates And Caps

Hard gates override the weighted score. A positive GMP, high retail subscription, or strong headline growth cannot override:

- Serious regulator, auditor, litigation, pledge, RPT, or related-party proceeds risk.
- Negative operating cash flow in two of three years while reporting profit.
- Material restatement or auditor qualification affecting revenue, inventory, receivables, related parties, or going concern.
- Pure or near-pure OFS with weak growth need and expensive valuation.
- SME risk stack dominated by GMP, weak disclosure, sudden profit spike, large RPTs, and no credible institutional filter.

Confidence is separate from the score:

- `High`: primary offer document parsed, official exchange data checked, peer set audited, and no major source conflicts.
- `Medium`: primary or official fallback data covers most fields, but a material source, table, or timestamp is missing.
- `Low`: secondary-only data, inaccessible primary documents, conflicting market signals, or early/intraday subscription without official category data.

If confidence is Low, final verdict should normally be `Neutral` or `Avoid`, not `Apply`, unless the user asks only for a narrow factual score with caveats.

## Required Output Fields

Every department score handoff should include:

```text
department_score: 0-100 or Unavailable
score_label: Strong / Moderate / Weak / Avoid-level risk
confidence: High / Medium / Low
evidence_quality: Primary / Official fallback / Mixed / Secondary-only
hard_gates: None or list
confidence_caps: None or list
missing_data: None or list
```
