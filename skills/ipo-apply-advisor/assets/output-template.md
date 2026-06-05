# IPO Apply Advisor Output Template

## Bias Check Result

- User bias: Apply / Avoid / Undecided / Not provided
- Bias adjustment: What evidence challenged that bias

## Decision Snapshot

| Field | Output |
|---|---|
| Decision | Apply / Avoid / Neutral |
| Best suited for | Listing gains / Long term / Both / Neither |
| Main reason | One sentence |
| Biggest risk | One sentence |
| Final score | X/100 / Provisional |
| Confidence | High / Medium / Low |

## Issue Context

| Field | Value |
|---|---|
| IPO |  |
| Classification | Mainboard / NSE Emerge / BSE SME / Unknown |
| Issue dates |  |
| Price band / fixed price |  |
| Lot size |  |
| Minimum amount |  |
| Fresh issue / OFS |  |
| Listing timeline | T+3 unless issue-specific timetable proves otherwise |

## Listing-Gain View

Cover GMP level/trend, QIB/NII/retail subscription, anchor quality, market context, issue size/float, SME liquidity, and valuation overhang.

## Long-Term Subscribe View

Cover business quality, financials, cash conversion, valuation, governance, use of proceeds, moat, and lock-in/overhang.

## Scorecard

| Component | Department score | Weight | Weighted contribution | Confidence / cap |
|---|---:|---:|---:|---|
| Financial quality | /100 | 25% | /25 | High / Medium / Low |
| Valuation / peer comparison | /100 | 20% | /20 | High / Medium / Low |
| Governance, red flags, issue structure | /100 | 20% | /20 | High / Medium / Low |
| Demand quality | /100 | 15% | /15 | High / Medium / Low |
| GMP / listing sentiment | /100 | 10% | /10 | High / Medium / Low |
| Application fit, liquidity, timeline risk | /100 | 10% | /10 | High / Medium / Low |
| Total |  | 100% | /100 | Apply / Neutral / Avoid zone |

Score status: Final / Provisional because [missing data, conflicting sources, official data unavailable].

Hard gates and confidence caps override the weighted score.

## Optional Shareable Dashboard

Include this section only when the user asks for a shareable dashboard, charts, chart-ready output, scorecard graphic brief, LinkedIn-ready dashboard, or similar output. Follow `references/dashboard-output.md`.

### Dashboard Status

| Field | Value |
|---|---|
| Dashboard status | Final / Provisional |
| Score status | Final / Provisional |
| Confidence | High / Medium / Low |
| Evidence quality | Primary / Official fallback / Mixed / Secondary-only |
| Do-not-overstate note | Missing data, source conflict, hard gate, or timestamp caveat |

### Verdict Card

| Field | Display |
|---|---|
| IPO |  |
| Decision | Apply / Neutral / Avoid |
| Final score | X/100 / Provisional |
| Confidence | High / Medium / Low |
| Best suited for | Listing gains / Long term / Both / Neither |
| Main reason | One evidence-backed sentence |
| Biggest risk | One evidence-backed sentence |
| Data status | Final / Provisional with reason |

### Weighted Score Dashboard

| Department | Score | Weight | Contribution | Confidence | Evidence quality | Source note |
|---|---:|---:|---:|---|---|---|
| Financial quality | /100 or Unavailable | 25% | /25 or Provisional | High / Medium / Low | Primary / Mixed / Secondary-only |  |
| Valuation / peer comparison | /100 or Unavailable | 20% | /20 or Provisional | High / Medium / Low | Primary / Mixed / Secondary-only |  |
| Governance, red flags, issue structure | /100 or Unavailable | 20% | /20 or Provisional | High / Medium / Low | Primary / Mixed / Secondary-only |  |
| Demand quality | /100 or Unavailable | 15% | /15 or Provisional | High / Medium / Low | Primary / Mixed / Secondary-only |  |
| GMP / listing sentiment | /100 or Unavailable | 10% | /10 or Provisional | High / Medium / Low | Primary / Mixed / Secondary-only |  |
| Application fit, liquidity, timeline risk | /100 or Unavailable | 10% | /10 or Provisional | High / Medium / Low | Primary / Mixed / Secondary-only |  |

### Text Bar Chart

```text
Financial quality                  [----------] X/100  Confidence
Valuation / peer comparison        [----------] X/100  Confidence
Governance / issue structure       [----------] X/100  Confidence
Demand quality                     [----------] X/100  Confidence
GMP / listing sentiment            [----------] X/100  Confidence
Application / liquidity / timeline [----------] X/100  Confidence
```

Use `[??????????] Unavailable` for missing departments. Do not score unavailable data as zero.

### Radar Chart Data

Provide valid JSON with actual scores or `null` for unavailable scores.

```json
{
  "chart_type": "radar",
  "scale": {"min": 0, "max": 100},
  "series": []
}
```

### Chart-Ready JSON

Provide valid JSON with IPO context, decision, departments, hard gates, confidence caps, source notes, and `not_financial_advice` set to `true`.

```json
{
  "ipo": {},
  "decision": {},
  "departments": [],
  "sources": []
}
```

### CSV Data Block

```csv
department,score,weight,weighted_contribution,confidence,evidence_quality,source_note
```

### Graphic Brief

- Format:
- Headline:
- Primary visual:
- Required badges:
- Footnote:

## Auto-Avoid / Red-Flag Check

State whether any hard gate fired. If yes, explain why the final decision remains Avoid even if GMP/subscription is positive.

## Contradictions

List major contradictions such as high GMP with weak QIB, strong fundamentals with expensive valuation, or SME hype with poor cash conversion.

Include market-signal conflicts such as zero GMP from one source and material premium from another, or secondary-only subscription without official category data.

## Category And Capital Required

State Retail / sHNI / bHNI / SME individual / Not recommended. Include amount and lot count when known. Flag ASBA/UPI/payment feasibility where relevant.

## Cut-Off Price

State Yes / No / Not available and explain using upper-band valuation and category rules.

## What Would Change The Verdict

| Direction | Evidence needed |
|---|---|
| More positive |  |
| More negative |  |

## Sources

| Source | Tier | Used for | Freshness / caveat |
|---|---|---|---|
|  |  |  |  |

## Verdict

| Field | Value |
|---|---|
| Decision | Apply / Avoid / Neutral |
| Confidence | High / Medium / Low |
| Bias adjusted | Yes / No |
| Category | Retail / sHNI / bHNI / Individual Investor |
| Amount needed | INR amount and lot count |
| Cut-off price | Yes / No / Not available |
