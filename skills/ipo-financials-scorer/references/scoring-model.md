# Financial Scoring Model

Use a financial-only 100-point score. Valuation, GMP, subscription, allotment odds, and final apply decisions are outside this score.

## Score Categories

| Category | Points | What it tests |
|---|---:|---|
| Growth durability | 18 | Revenue CAGR, PAT/EBITDA trend, growth quality. |
| Profitability | 18 | EBITDA margin, PAT margin, margin stability, sector fit. |
| Return efficiency | 16 | ROCE, ROE/RoNW, RoA where relevant. |
| Cash conversion | 16 | CFO/PAT, cumulative CFO/PAT, FCF, CFO trend. |
| Balance-sheet strength | 14 | D/E, net debt/EBITDA, interest cover, net cash, liquidity. |
| Working-capital discipline | 10 | NWC days, CCC, DSO/DIO/DPO trend. |
| Disclosure and earnings quality | 8 | Restatement quality, auditor flags, one-offs, concentration, RPT impact. |

## Labels

| Raw score | Label |
|---:|---|
| 75-100 | Strong, unless capped by override. |
| 55-74 | Moderate. |
| 30-54 | Weak. |
| 0-29 | Avoid-level financial risk. |

Caps override the raw label. Show both raw score and cap reason.

## Growth Durability - 18

| Condition | Points |
|---|---:|
| Revenue CAGR above 20%, latest-year growth positive, no major quality concern | 18 |
| Revenue CAGR 15-20% | 14 |
| Revenue CAGR 10-15% | 10 |
| Revenue CAGR 5-10% | 6 |
| Revenue CAGR 0-5% | 3 |
| Declining revenue | 0 |

Adjust within the category:

- Add up to 2 points for EBITDA/PAT improving faster than revenue.
- Subtract 2-5 points for acquisition-led, commodity-led, or receivable-led growth.
- For cyclicals, consider cycle-normalized revenue and utilization instead of one peak year.

## Profitability - 18

Generic non-financial companies:

| Condition | Points |
|---|---:|
| EBITDA margin above 18% and PAT margin above 10%, stable or improving | 18 |
| EBITDA margin 12-18% and PAT margin 6-10% | 13 |
| EBITDA margin 8-12% and PAT margin 3-6% | 8 |
| Positive EBITDA but weak PAT margin | 4 |
| Negative EBITDA or recurring losses without clear improvement | 0 |

Use sector tables for banks/NBFCs, SaaS, infra/EPC, retail/QSR, and manufacturing instead of applying generic margin cutoffs mechanically.

## Return Efficiency - 16

Generic non-financial companies:

| Condition | Points |
|---|---:|
| ROCE above 20% and ROE above 18% without excessive leverage | 16 |
| ROCE 15-20% and ROE 12-18% | 12 |
| ROCE 10-15% or ROE 8-12% | 7 |
| ROCE 6-10% or ROE 4-8% | 3 |
| ROCE below 6%, negative, or not meaningful due to losses | 0 |

Caps:

- If ROE is high only because net worth is tiny or debt is high, cap return-efficiency points at 8.
- Score historical efficiency separately from post-issue dilution.
- For banks/NBFCs, use RoA, RoE, capital adequacy, and asset quality.

## Cash Conversion - 16

| Condition | Points |
|---|---:|
| 3-year cumulative CFO/PAT above 1.0 and latest CFO positive | 16 |
| Cumulative CFO/PAT 0.75-1.0 | 12 |
| Cumulative CFO/PAT 0.5-0.75 | 8 |
| Cumulative CFO/PAT 0.25-0.5 | 4 |
| Negative cumulative CFO, or CFO negative in 2+ years despite profits | 0 |

Adjustments:

- If PAT is negative, use CFO/EBITDA, FCF trend, burn, and runway.
- If CFO is strong only because payables stretched sharply, do not award full points.
- If working-capital funding is a major IPO object, cap cash-conversion points at 10 unless the cycle is clearly improving.

## Balance-Sheet Strength - 14

Generic non-financial companies:

| Condition | Points |
|---|---:|
| Net cash or D/E below 0.3 and interest cover above 6x | 14 |
| D/E 0.3-0.8 and interest cover above 4x | 11 |
| D/E 0.8-1.5 and interest cover above 2.5x | 7 |
| D/E 1.5-3.0 or interest cover 1.5-2.5x | 3 |
| D/E above 3.0, interest cover below 1.5x, or negative net worth | 0 |

For debt repayment IPOs, show pre-issue and post-repayment leverage when disclosed.

## Working-Capital Discipline - 10

| Condition | Points |
|---|---:|
| NWC days or CCC low/stable and cash conversion healthy | 10 |
| NWC days manageable with no receivable/inventory stress | 7 |
| Elevated but explainable working capital | 4 |
| Deteriorating receivables, inventory, or payables stress | 1 |
| Severe cash-cycle stress or uncollectable working-capital signs | 0 |

Use business-model judgment. Negative working capital may be strong for retail/SaaS if customer advances and deferred revenue are durable; it can be weak if it reflects delayed supplier payments.

## Disclosure and Earnings Quality - 8

| Condition | Points |
|---|---:|
| Clean restatement, certified KPIs, clear formulas, low one-off/RPT risk | 8 |
| Mostly clear disclosures with minor formula gaps | 6 |
| Several missing KPIs, one-offs, or limited segment detail | 4 |
| Material unexplained one-offs, RPTs, concentration, or restatement concerns | 1 |
| Auditor/going concern/revenue recognition issue affecting statements | 0 |

Do not let this category alone hide a critical override; apply caps separately.
