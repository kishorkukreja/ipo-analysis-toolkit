# IPO Listing Day Strategy Output Template

## Data Freshness

| Field | Value |
|---|---|
| Checked at | `[YYYY-MM-DD HH:MM IST or "not live-checked"]` |
| Sources checked | `[NSE/BSE/SEBI/offer document/aggregators/user-provided]` |
| Missing data | `[None or list]` |
| Data status | `[Live / Recent / User-provided / Hypothetical / Incomplete]` |

## Listing Setup

| Field | Value |
|---|---|
| Company / symbol |  |
| Exchange / platform | `[NSE/BSE mainboard, NSE Emerge, BSE SME, unknown]` |
| Issue price | `Rs` |
| Lot size / allotted quantity |  |
| Listing timeline | `T+3 unless older issue facts say otherwise` |
| User intent | `[listing gain / 3-6 month hold / long-term hold / unknown]` |

## Live Or Scenario Signal

| Field | Value |
|---|---|
| IEP |  |
| IEP vs issue price |  |
| Indicative quantity / depth |  |
| Cancelled orders |  |
| Signal label | `[Strong / Moderate / Weak / Unreliable]` |
| Application/liquidity/timeline score | `X/100` |
| Signal caveat |  |

## Input Scorecard

| Input | Read | Interpretation | Action effect |
|---|---|---|---|
| GMP |  | Informal/unregulated; reliability `[Low/Moderate]` |  |
| Subscription |  | QIB/NII/Retail/overall quality |  |
| Valuation/fundamentals |  | Cheap/fair/rich and key red flags |  |
| Market mood |  | Nifty/sector/breadth |  |
| SME liquidity |  | Required warning if SME |  |

## Strategy

| Field | Recommendation |
|---|---|
| Recommended action | `[Sell all / Sell majority / Sell partial / Hold with stop / Avoid secondary buy]` |
| Sell now | `% or shares/lots` |
| Hold | `% or shares/lots` |
| Stop-loss / exit trigger |  |
| First-hour review trigger |  |
| Order style | `Limit orders for SPOS/thin SME; avoid market orders where depth is poor` |

## Net Outcome

| Field | Estimate |
|---|---|
| Gross gain/loss |  |
| STT on sale |  |
| Approx STCG tax |  |
| Approx net before brokerage |  |
| Tax caveat | `Not tax advice; actual tax depends on investor facts and charges.` |

## Scenario Table

| Scenario | Action |
|---|---|
| Opens higher than IEP |  |
| Opens around IEP |  |
| Breaks issue price |  |
| Rallies after first 15 minutes |  |

## Verdict

| Field | Result |
|---|---|
| Action |  |
| Confidence | `[High / Medium / Low]` |
| Suggested sell now |  |
| Suggested hold |  |
| Stop-loss |  |
| Listing signal | `[Strong / Moderate / Weak / Unreliable]` |
| Main risk | `[Liquidity / valuation / weak QIB / market selloff / GMP mismatch / missing live data]` |

## Advisor Handoff

| Field | Value |
|---|---|
| department_score | X/100 |
| score_label | Positive / Neutral / Negative / Unreliable |
| confidence | High / Medium / Low |
| evidence_quality | Live exchange / Official fallback / Mixed / Secondary-only |
| hard_gates | None / list |
| confidence_caps | None / missing live data / thin liquidity / SME |
| missing_data | None / list |

This is a listing-day decision framework, not personalized investment advice.
