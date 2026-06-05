# [Company] IPO Subscription Tracker

## Snapshot

| Field | Value |
|---|---|
| IPO type | Mainboard / NSE SME / BSE SME / Unknown |
| Listing platform | NSE / BSE / NSE Emerge / BSE SME / Unknown |
| Issue dates | YYYY-MM-DD to YYYY-MM-DD |
| Price band | Rs X-Rs Y / Fixed price Rs X / Not verified |
| Lot size | X shares / Not verified |
| Minimum application amount | Rs X / Not verified |
| Data status | Live/intraday / Near close / Final exchange update / Post basis-of-allotment / Not verified |
| IPO stage | Pre-open / Day 1 / Middle days / Final day / Post-close pre-allotment / Post-allotment pre-listing / Listed |
| Data fetched | YYYY-MM-DD HH:MM IST |
| Source timestamp | YYYY-MM-DD HH:MM IST / Not shown |
| Timeline note | T+3 working days from issue close for current public issues |

## Source Checks

| Source | Type | What was checked | Timestamp | Status |
|---|---|---|---|---|
| NSE/BSE issue page | Primary | Subscription, dates, lot size |  | Checked / Missing |
| Exchange announcements | Primary | Anchor allotment, issue documents |  | Checked / Missing |
| Basis of allotment / registrar | Primary | Final applications/allotment |  | Checked / Not yet available |
| Aggregator | Secondary | Day-wise trend/cross-check |  | Used / Not used |

## Subscription

| Category | Offered | Bid | Subscription | Signal |
|---|---:|---:|---:|---|
| QIB |  |  |  | Institutional demand |
| NII/HNI total |  |  |  | High-net-worth demand; interpret cautiously |
| sHNI/sNII |  |  |  | Split if available |
| bHNI/bNII |  |  |  | Split if available |
| Retail/RII |  |  |  | Public demand and lottery odds |
| Employee |  |  |  | Issue-specific |
| Reserved/Other |  |  |  | Do not merge into retail |
| Total |  |  |  | Overall demand |

## Day-Wise Trend

| Day/status | QIB | NII/HNI | Retail/RII | Total | Source/timestamp | Note |
|---|---:|---:|---:|---:|---|---|
| Day 1 |  |  |  |  |  | Preliminary |
| Day 2 |  |  |  |  |  |  |
| Final day |  |  |  |  |  | Intraday or final must be stated |

## Anchor Book

| Metric | Value |
|---|---|
| Anchor amount | Rs X crore / Not found |
| Number of anchors/schemes | X / Not found |
| Domestic MF participation | Strong / Mixed / Weak / Not verified |
| Notable anchors |  |
| Concentration | Low / Medium / High / Not verified |
| Quality score | X/10 / Not scored |
| Lock-in note | 50% locked 30 days, 50% locked 90 days, if current rules apply |

## Retail Allotment Estimate

| Field | Value |
|---|---|
| Available retail shares/lots |  |
| Valid retail applications |  |
| Retail subscription multiple |  |
| Estimated chance |  |
| Method | Exact from valid applications / Proxy from subscription multiple / Not enough data |
| Caveat | Estimate only; final probability depends on valid applications and basis of allotment |

## Cutoff vs Price Bidding

| Question | Answer |
|---|---|
| Is cutoff bidding available? | Yes / No / Not verified |
| Best retail framing |  |
| Specific price risk |  |
| SME process check | Required for SME issues, especially opening on or after 2025-07-01 |

## Interpretation

| Field | Value |
|---|---|
| Demand quality score | X/100 |
| Demand quality | Strong / Mixed / Weak |
| Allotment odds | High / Moderate / Low / Very low / Long-shot |
| Data confidence | High / Medium / Low |
| Official data missing | Yes / No |
| Early-stage caveat applied | Yes / No |
| Main driver | QIB / Retail / NII / Anchor / Mixed / Unknown |

## Source Reconciliation

- Official-source agreement:
- Secondary-source differences:
- Missing or stale fields:
- Whether final data is confirmed:

## Investor Takeaway

- Demand quality:
- Retail implication:
- HNI/NII implication:
- Anchor implication:
- Timeline implication:

## Advisor Handoff

| Field | Value |
|---|---|
| department_score | X/100 |
| score_label | Strong / Mixed / Weak |
| confidence | High / Medium / Low |
| evidence_quality | Official exchange / Official fallback / Mixed / Secondary-only |
| hard_gates | None / weak QIB with hype / other |
| confidence_caps | None / early-stage / secondary-only / timestamp missing |
| missing_data | None / list |

## Caveats and Missing Data

- Subscription is a demand signal, not a complete investment decision.
- Day 1/opening-day subscription is preliminary; do not over-weight retail/NII before final-day QIB behavior is visible.
- GMP, if mentioned, is informal and unregulated and must stay separate from official subscription.
- Live data can change sharply near close.
- No allotment, listing gain, or return is guaranteed.
- Missing data:
