# IPO Financials Scorecard: [Company] IPO

## Financial Verdict

| Metric | Result |
|---|---|
| IPO classification | [Mainboard / NSE Emerge / BSE SME] |
| Issue open date | [YYYY-MM-DD / Not available] |
| Financial score | [score]/100 |
| Financial score label | [Strong / Moderate / Weak / Avoid-level financial risk] |
| Confidence | [High / Medium / Low] |
| Evidence quality | [Primary / Official fallback / Mixed / Secondary-only] |
| Sector model | [Generic / Manufacturing / Retail / Infra-EPC / Bank-NBFC / SaaS / Other] |
| SME adjustment | [Yes / No / Not applicable] |
| Score cap applied | [No / Yes - reason] |
| Data freshness | [Checked YYYY-MM-DD, source timestamp if available] |

## Source Check

| Source type | Source used | Status | Caveat |
|---|---|---|---|
| Primary offer document | [DRHP/RHP/prospectus URL] | [Used / Missing / Inaccessible] | [Restated consolidated financials preferred] |
| Abridged prospectus | [URL / Not used] | [Navigation only / Fallback] | [Cross-check required if fallback] |
| Exchange/SEBI page | [URL] | [Used / Missing] | [Classification/date context] |
| Secondary source | [URL / None] | [Fallback only] | [Confidence impact] |

## Score Breakdown

| Category | Points | Max | Rationale |
|---|---:|---:|---|
| Growth durability | [ ] | 18 | [Revenue CAGR, latest trend, growth quality.] |
| Profitability | [ ] | 18 | [EBITDA/PAT margin trend and sector fit.] |
| Return efficiency | [ ] | 16 | [ROCE, ROE/RoNW, or sector substitutes.] |
| Cash conversion | [ ] | 16 | [CFO/PAT, cumulative conversion, FCF.] |
| Balance-sheet strength | [ ] | 14 | [D/E, net debt/EBITDA, interest cover, liquidity.] |
| Working-capital discipline | [ ] | 10 | [NWC days, CCC, DSO/DIO/DPO, sector interpretation.] |
| Disclosure and earnings quality | [ ] | 8 | [Restatement quality, KPIs, one-offs, RPTs, audit flags.] |
| Total | [ ] | 100 | [Raw score before caps.] |

## Key Financials

| Rs crore unless stated | FY[oldest] | FY[middle] | FY[latest] | Stub period | Trend |
|---|---:|---:|---:|---:|---|
| Revenue from operations | [ ] | [ ] | [ ] | [ ] | [ ] |
| EBITDA | [ ] | [ ] | [ ] | [ ] | [reported/computed] |
| PAT | [ ] | [ ] | [ ] | [ ] | [ ] |
| CFO | [ ] | [ ] | [ ] | [ ] | [ ] |
| Gross debt | [ ] | [ ] | [ ] | [not annualized] | [ ] |
| Net worth | [ ] | [ ] | [ ] | [not annualized] | [ ] |

## Ratio Calculations

| Ratio | Formula used | Latest full year | 3-year view | Interpretation |
|---|---|---:|---|---|
| Revenue CAGR | [latest/oldest over intervals] | [ ] | [ ] | [ ] |
| EBITDA margin | EBITDA / revenue | [ ] | [ ] | [ ] |
| PAT margin | PAT / revenue | [ ] | [ ] | [ ] |
| ROCE | [formula used] | [ ] | [ ] | [ ] |
| ROE/RoNW | [formula used] | [ ] | [ ] | [ ] |
| Debt-to-equity | Gross debt / net worth | [ ] | [ ] | [ ] |
| Interest coverage | EBIT / finance cost | [ ] | [ ] | [ ] |
| CFO/PAT | CFO / PAT | [ ] | [cumulative] | [ ] |
| NWC days / CCC | [formula used] | [ ] | [ ] | [ ] |

## Issuer KPIs vs Skill-Computed Metrics

| Metric | Issuer reported | Skill computed | Difference / caveat |
|---|---:|---:|---|
| [KPI] | [ ] | [ ] | [reported_by_issuer / computed_by_skill / both] |

## Sector-Specific Checks

| Check | Result | Implication |
|---|---|---|
| [Capacity utilization / asset quality / order book / SSSG / unit economics] | [ ] | [ ] |
| Customer concentration | [ ] | [ ] |
| Related-party financial impact | [ ] | [ ] |

## Normalizations and Data Quality

- Financial source: [Restated consolidated / standalone / secondary fallback].
- Units normalized to: [Rs crore / other].
- Stub period treatment: [none / shown separately / annualized with caveat].
- Growth quality: [clean / partly normalized / distorted].
- Formula differences: [issuer formula differs from skill formula / none found].
- Missing data: [items and score impact].

## Overrides

| Override type | Applied | Reason | Label impact |
|---|---|---|---|
| Critical | [Yes/No] | [ ] | [ ] |
| Serious | [Yes/No] | [ ] | [ ] |
| Positive modifier | [Yes/No] | [ ] | [confidence/rationale only] |

## Retail Investor Implications

- [Plain-language implication of growth, profitability, returns, cash conversion, leverage, and working capital.]
- This is a financial-quality score, not an application recommendation.
- Valuation, GMP, subscription, and allotment odds require separate analysis.

## Handoff Fields

| Field | Value |
|---|---|
| financial_score | [number] |
| financial_label | [Strong / Moderate / Weak / Avoid-level financial risk] |
| confidence | [High / Medium / Low] |
| ipo_classification | [Mainboard / NSE Emerge / BSE SME] |
| sector_model | [ ] |
| cash_conversion_quality | [Strong / Mixed / Weak] |
| leverage_risk | [Low / Medium / High] |
| working_capital_risk | [Low / Medium / High] |
| disclosure_quality | [Strong / Adequate / Weak] |
| loss_making | [Yes / No] |
| sme_adjustment_applied | [Yes / No / Not applicable] |
| critical_financial_red_flags | [None / list] |
| hard_gates | [None / list] |
| confidence_caps | [None / list] |
| missing_data | [None / list] |
