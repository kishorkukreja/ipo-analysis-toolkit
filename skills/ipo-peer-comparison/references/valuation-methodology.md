# Valuation Methodology

## Multiple Selection

Choose the primary metric from the business model. P/E is not universal.

| Multiple | Use when | Avoid when |
|---|---|---|
| P/E | Profitable, stable earnings, comparable tax/depreciation/leverage | Loss-making, one-off PAT, cyclically inflated EPS, high leverage mismatch |
| P/B | Banks, NBFCs, insurers, asset-heavy financials, real estate | Asset-light operating companies |
| EV/EBITDA | Manufacturing, hospitals, diagnostics, hotels, logistics, capital goods, infrastructure operations | Banks, insurers, negative EBITDA, distorted lease accounting |
| EV/EBIT | Capital-intensive businesses where depreciation matters | Early-stage or loss-making issuers |
| P/S or EV/Sales | Loss-making, SaaS/platforms, high-growth retail, temporarily depressed EBITDA | Mature low-growth companies with poor unit economics |
| EV/AUM or P/AUM | AMCs, wealth managers, some lending/AUM models | Non-financial operating companies |
| P/Embedded Value | Life insurers | General insurers, banks, non-insurers |
| NAV premium/discount | Real estate, asset pools, REIT/InvIT-like structures | Asset-light businesses |

Always pair the multiple with business-quality checks. A low multiple is not automatically cheap, and a high multiple is not justified without evidence.

## Formulae

- `IPO P/E = issue price / restated diluted EPS`
- `P/B = market capitalization / net worth`
- `Enterprise Value = equity value + total debt + lease liabilities + minority interest + preferred shares - cash and cash equivalents`
- `EV/EBITDA = enterprise value / EBITDA`
- `P/S = equity value / revenue`
- `EV/Sales = enterprise value / revenue`
- `Premium/discount = (IPO multiple / peer median multiple) - 1`

Use the upper price band by default because retail applications usually bid at cut-off and valuation risk should be tested at the highest price.

## Peer Benchmarking

Show:

- IPO multiple.
- Peer low, high, median, and mean when the peer set is clean.
- Peer count and excluded peers.
- Premium/discount to peer median.
- Whether the IPO multiple is inside, below, or above the peer range.

Use median as the headline because average can be distorted by outliers.

## Verdict Bands

Start with the primary multiple, then adjust for business quality.

| Premium/discount to primary peer median | Base interpretation |
|---:|---|
| More than 25% discount | Undervalued if no major quality issue |
| 10% to 25% discount | Attractively priced |
| -10% to +10% | Fairly priced |
| +10% to +25% | Premium pricing; needs justification |
| +25% to +50% | Expensive; strong growth/quality required |
| More than +50% | Overvalued unless exceptional evidence |

Allowed verdicts:

- `Undervalued`
- `Fairly priced`
- `Expensive but justified`
- `Overvalued`
- `Speculative / low confidence`
- `Value trap risk` when discount exists but quality is weak.

## Adjustment Logic

Growth premium:

- 0 to +5 pp revenue CAGR spread: 0% to +5% possible premium.
- +5 to +15 pp: +5% to +15% possible premium.
- +15 to +30 pp: +15% to +30% possible premium.
- More than +30 pp: cap around +30% unless margins, cash flow, and unit economics are credible.

Reject or cap growth premiums when revenue growth is acquisition-led, customer-concentrated, discount-led, working capital consumes cash, OCF is negative despite PAT growth, or margins are falling.

Margin and quality:

- Higher growth plus higher margin can justify a premium.
- Higher growth plus lower margin requires a credible expansion path.
- Lower growth plus higher margin can support a fair multiple.
- Lower growth plus lower margin requires a discount.

Scale and liquidity:

- Revenue > 0.7x peer median: 0% to -5% adjustment.
- Revenue 0.3x to 0.7x peer median: -5% to -15%.
- Revenue < 0.3x peer median: -15% to -30%.
- SME with thin float or lot-size friction: additional -10% to -25%.

Issue structure:

- Fresh issue for debt repayment or growth capex can improve post-issue EV and balance-sheet risk.
- Pure or OFS-heavy issues do not add growth capital.
- OFS-heavy IPOs priced at a premium to peers deserve stricter caveats.

Leverage:

- Use EV multiples where debt differs materially.
- If proceeds repay debt, show pre-issue and post-issue leverage/EV assumptions.
- Do not give full credit for debt repayment when the model is structurally working-capital intensive.

## Sector Map

| Sector | Primary metrics | Supporting checks |
|---|---|---|
| IT services | P/E, EV/EBITDA | EBIT margin, growth, client/geography concentration |
| SaaS/platform | EV/Sales, P/S, ARR/KPI multiples | Gross margin, NRR, churn, CAC payback, path to EBITDA |
| Consumer/retail | P/E, EV/EBITDA, P/S | Store economics, SSSG, gross margin, working capital |
| Manufacturing/capital goods | EV/EBITDA, P/E | ROCE, order book, capex, working capital, debt |
| Chemicals/pharma | EV/EBITDA, P/E | Export mix, molecule/product concentration, cycle position |
| Banks/NBFC/HFC/MFI | P/B, P/adjusted book | ROA, ROE, GNPA/NNPA, credit cost, NIM, CAR |
| AMC/wealth | EV/AUM, P/E | AUM mix, yields, flows, market share, margins |
| Life insurance | P/EV | VNB margin, APE growth, persistency, solvency |
| General insurance | P/B, P/GWP | Combined ratio, claims ratio, solvency, investment income |
| Real estate | NAV premium/discount, P/B | Net debt, pre-sales, collections, approvals, inventory |
| Logistics | EV/EBITDA | Utilization, asset-light/fleet mix, fuel pass-through |
| Power/renewables/infrastructure | EV/EBITDA, P/B, NAV/DCF | PPA tenor, counterparty, debt, receivables, PLF/CUF |

## Special Ratio Rules

- If EPS is negative, mark P/E `Not meaningful`; never report P/E as zero.
- If EBITDA is negative, mark EV/EBITDA `Not meaningful` and use EV/Sales, gross profit, or KPIs.
- If latest PAT has exceptional income, show reported and adjusted P/E.
- For cyclicals, avoid "cheap" claims based only on peak-cycle earnings; use mid-cycle context where possible.
- For newly profitable issuers, pair P/E with P/S or EV/Sales and flag short profit history.
