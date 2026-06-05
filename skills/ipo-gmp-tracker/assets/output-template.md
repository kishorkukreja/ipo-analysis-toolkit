# IPO GMP Tracker Output Template

## GMP Snapshot

| Field | Value |
|---|---|
| IPO |  |
| Classification | Mainboard / NSE SME / BSE SME / Unknown |
| Issue open date | YYYY-MM-DD / Not found |
| Issue close date | YYYY-MM-DD / Not found |
| Listing timeline | T+3 working days from close, or issue-specific rule |
| Issue price used | INR X upper band / fixed price / Not found |
| Lot size | X shares / Not found |
| Current GMP | INR X per share / Not available |
| GMP range | INR X-INR Y / Not applicable |
| Conflict flag | Yes / No |
| GMP % | X.X% / Not calculable |
| Implied listing price | INR X / Range / Not calculable |
| Implied gain/loss per lot | INR X / Not calculable |
| Data freshness | Fresh / Acceptable / Stale / Unknown |

## Source Cross-Check

| Source | URL | GMP | Updated | Use In Analysis | Notes |
|---|---|---:|---|---|---|
| Chittorgarh |  |  |  | Included / Excluded / Not found |  |
| InvestorGain |  |  |  | Included / Excluded / Not found |  |
| IPOWatch |  |  |  | Included / Excluded / Not found |  |

## Trend

| Stage | Date/Time | GMP | Source | Note |
|---|---|---:|---|---|
| Pre-open |  |  |  |  |
| Day 1 |  |  |  |  |
| Day 2 |  |  |  |  |
| Final day |  |  |  |  |
| Post-close |  |  |  |  |
| Allotment day |  |  |  |  |
| Final 24-48h |  |  |  |  |
| Listing morning |  |  |  |  |

Trend classification: Rising steadily / Rising sharply / Flat positive / Flat zero / Falling from high / Volatile / Divergent / Unknown.

## Subscription And Context Check

| Field | Value |
|---|---|
| Total subscription |  |
| QIB subscription |  |
| NII/HNI subscription |  |
| Retail subscription |  |
| Anchor or institutional note |  |
| Market context |  |
| SME liquidity note | Required for SME, otherwise Not applicable |

## Reliability

| Field | Value |
|---|---|
| Score | X/100 |
| Label | High / Medium / Low / Very Low |
| Department score for advisor | X/100 |
| Main drivers | Source agreement, freshness, trend, subscription support, market context |
| Caps applied | One source / SME one-source / stale data / weak QIB / source divergence / manipulation risk / None |

## Conflict Handling

| Field | Value |
|---|---|
| Source spread | INR X or X% of issue price |
| Zero-vs-premium conflict | Yes / No |
| Range used for implied listing | Yes / No |
| Advisor handoff | Treat GMP score as provisional / Usable with caveats / Not usable |

## Advisor Handoff

| Field | Value |
|---|---|
| department_score | X/100 |
| score_label | Strong / Noisy / Weak / Not usable |
| confidence | High / Medium / Low |
| evidence_quality | Primary for IPO basics plus GMP secondary / Mixed / Secondary-only |
| hard_gates | None / manipulation or promotional warning |
| confidence_caps | None / list |
| missing_data | None / list |

## Facts

- 

## Interpretation

- 

## Retail Investor Implications

- GMP is one listing-sentiment input only.
- Do not apply or avoid solely because of GMP.
- Use `ipo-apply-advisor` or a fuller analysis for fundamentals, valuation, red flags, subscription, allotment odds, and risk fit.

## Caveats And Missing Data

- GMP is informal, unregulated, and not guaranteed.
- Actual listing price can differ materially from implied GMP.
- Missing or stale fields:
- For SME IPOs, positive GMP does not remove liquidity, spread, lot-size, and exit-risk constraints.

## Sources

- 
