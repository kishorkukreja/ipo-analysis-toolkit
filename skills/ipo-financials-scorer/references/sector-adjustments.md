# Sector and SME Adjustments

Use this file after the base score. Sector models adjust metric interpretation; they do not permit unsupported investment advice.

## Banks, NBFCs, and Financial Services

Replace EBITDA, conventional D/E, ROCE, and working-capital cycle with financial-sector metrics.

Primary metrics:

| Metric | Strong | Moderate | Weak |
|---|---|---|---|
| RoA | Above 1.5% | 0.8-1.5% | Below 0.8% or losses |
| RoE | Above 15% | 10-15% | Below 10% |
| GNPA/NNPA | Low and improving | Stable but elevated | Deteriorating |
| Provision coverage | Strong | Adequate | Weak |
| Capital adequacy | Comfortable buffer | Adequate | Near/below requirement |
| NIM/spread | Stable or improving | Stable | Compressing sharply |

Overrides:

- Cap at `Weak` if regulatory capital is near or below requirement without credible post-issue buffer.
- Cap at `Weak` if asset quality is deteriorating sharply with weak provision cover.
- Use RBI/regulatory disclosures and offer-document risk factors for current context.

## SaaS, Digital Platforms, and New-Age Tech

Traditional PAT scoring may be misleading for scaling businesses.

Primary metrics:

| Metric | Strong | Moderate | Weak |
|---|---|---|---|
| Revenue growth | High and retained | Good but slowing | Slowing sharply |
| Gross margin | High and stable | Acceptable | Weak or falling |
| Contribution margin | Positive/improving | Improving | Negative/unclear |
| EBITDA/FCF trend | Clear path to break-even | Losses narrowing | Losses widening |
| Rule of 40 | Around/above 40 when mature | 20-40 | Below 20 |
| Runway | Above 24 months | 12-24 months | Below 12 months |

Caps:

- Max `Strong` only with high-quality recurring/retained revenue, strong gross margin, improving contribution margin, visible EBITDA break-even path, and post-issue runway above 24 months.
- Cap at `Moderate` if cohort, retention, or unit-economics disclosure is missing.
- Cap at `Weak` if revenue growth slows while EBITDA/FCF losses remain large.

## Infrastructure, EPC, Construction, and Real Estate

Revenue CAGR alone is weak evidence because execution cycles, receivables, and order book quality dominate.

Primary metrics:

| Metric | Strong | Moderate | Weak |
|---|---|---|---|
| Order book/revenue | Above 3x and executable | 2-3x | Below 2x or slow/stuck |
| EBITDA margin | Above 12% EPC; above 20% real estate | 8-12% EPC | Below 8% EPC |
| Interest cover | Above 4x | 2-4x | Below 2x |
| Net debt/EBITDA | Below 2x | 2-4x | Above 4x |
| NWC days | Stable/sector-normal | Elevated but funded | Stretching sharply |
| ROCE | Above 15% | 10-15% | Below 10% |

Extract order book, execution period, client mix, receivables, contract assets, retention money, mobilisation advances, SPV guarantees, contingent claims, land bank, pre-sales, collections, and RERA status where relevant.

Caps:

- Cap at `Weak` if CFO is persistently negative and working capital is funded by short-term debt.
- Cap at `Moderate` if order book is high but concentrated in slow-moving projects.
- Cap at `Weak` if material promoter-linked receivables or related-party subcontracting are unexplained.

## Retail, QSR, Consumer, and Distribution

Low PAT margin can still be acceptable when store economics and cash conversion are strong.

Primary metrics:

| Metric | Strong | Moderate | Weak |
|---|---|---|---|
| Same-store sales growth | Above inflation plus category growth | Around category | Negative |
| Revenue CAGR | Above 20% with productivity | 10-20% | Below 10% |
| Gross margin | Stable/improving | Stable low | Declining |
| EBITDA margin | Above 10-12% | 6-10% | Below 6% |
| Inventory turns | Improving/fast | Stable | Slow/obsolete |
| CCC | Negative or low, sustainable | Moderate | Stretching |
| Store payback | Below 3 years | 3-5 years | Above 5 years or undisclosed |

Caps:

- Cap at `Moderate` if growth is mainly new stores and mature-store performance is weak.
- Cap at `Weak` if inventory grows materially faster than sales with weak CFO.
- Cap at `Weak` if customer advances or payables fund losses without credible margin path.

## Manufacturing, Industrials, Auto Ancillaries, Chemicals, and Textiles

Emphasize capacity, utilization, operating leverage, raw-material pass-through, customer concentration, working capital, and ROCE.

Primary metrics:

| Metric | Strong | Moderate | Weak |
|---|---|---|---|
| Revenue CAGR | Above 15% volume-backed | 8-15% | Below 8% |
| EBITDA margin | Above 15% | 10-15% | Below 10% |
| ROCE | Above 18% | 12-18% | Below 12% |
| Capacity utilization | Above 75% with expansion plan | 50-75% | Below 50% or unclear |
| D/E | Below 0.7 | 0.7-1.5 | Above 1.5 |
| CFO/PAT | Above 0.8 cumulative | 0.5-0.8 | Below 0.5 |
| Working capital | Stable | Manageable | Receivable/inventory stress |

Caps:

- Cap at `Moderate` if customer concentration is high even with strong margins.
- Cap at `Weak` if rapid growth is mostly receivables-led.
- Cap at `Weak` if IPO proceeds fund capex but current utilization is low and demand evidence is weak.

## Loss-Making IPOs

Rules:

- PAT CAGR is `not meaningful` when endpoint losses make CAGR misleading.
- PAT margin should be shown as a trend, not as the whole score.
- ROE/ROCE may be negative or not meaningful; use gross margin, contribution margin, EBITDA trend, burn/runway, and unit economics.
- OCF/PAT is not meaningful when PAT is negative; use CFO/EBITDA, FCF burn, and runway.
- P/E and valuation are outside this skill.

Caps:

- Max `Strong` only if revenue quality, gross margin, contribution margin, break-even path, and runway are all strong.
- Max `Moderate` if losses narrow but unit economics or retention are incomplete.
- Max `Weak` if growth slows while losses and cash burn remain high.
- Max `Weak` if IPO proceeds mainly fund losses/general corporate purposes without a clear operating leverage path.

Output additions:

- Path to profitability: Clear / Plausible / Unclear.
- Burn runway: months, if calculable.
- Unit economics disclosed: Yes / Partial / No.
- Loss score cap applied: Yes / No, with reason.

## SME IPO Adjustments

SME IPOs use the same 100-point score, but confidence and caps are stricter.

Required additions:

- SME adjustment applied: Yes / No.
- Scale risk: Low / Medium / High.
- Disclosure confidence: High / Medium / Low.
- Cash collection quality: Strong / Mixed / Weak.

Rules:

- Require stronger cash conversion for a `Strong` label.
- Penalize customer concentration more heavily.
- Penalize related-party revenue, purchases, leases, loans, and guarantees more heavily.
- Treat sudden pre-IPO growth spurts skeptically unless backed by cash collection and capacity evidence.
- If Accounting Standards rather than Ind AS are used, caveat peer comparisons.
- If fewer than three full years of comparable operations are available, cap at `Moderate` unless exceptionally clean and profitable.

SME caps:

- Cap at `Moderate` if top-customer revenue exceeds 40% unless long-term contract and payment history are strong.
- Cap at `Weak` if CFO is negative in the latest year despite PAT, unless clearly temporary and funded.
- Cap at `Weak` if auditor qualifications, aggressive restatements, or unexplained related-party flows exist.
- Cap at `Moderate` if scale is very small and margins are materially above sector without explanation.
