# Metric Formulas

## Growth

Revenue CAGR:

```text
((latest_full_year_revenue / oldest_full_year_revenue) ^ (1 / years_between) - 1) * 100
```

For FY2023 to FY2025, use two intervals.

PAT CAGR:

- Compute only when oldest and latest full-year PAT are positive and not near zero.
- If either endpoint is negative, show `not meaningful` and score using loss-making trend rules.
- For loss-to-profit transitions, show absolute improvement and latest PAT margin.

Growth quality:

- `clean`: broad-based and cash-supported.
- `partly normalized`: affected by acquisition, commodity price, currency, one-off contracts, or base effects but still usable.
- `distorted`: growth number is materially misleading without adjustment.

## Profitability

```text
Gross margin = (Revenue from operations - COGS) / Revenue from operations * 100
EBITDA margin = EBITDA / Revenue from operations * 100
PAT margin = PAT / Revenue from operations * 100
```

If the issuer uses total income as denominator, disclose the difference.

## Returns

Preferred ROE:

```text
PAT attributable to equity shareholders / average equity attributable to owners * 100
```

Common offer-document RoNW:

```text
PAT / year-end net worth * 100
```

Preferred ROCE:

```text
EBIT / average capital employed * 100
capital employed = total equity + total borrowings - cash and cash equivalents
```

Alternative ROCE denominator:

```text
capital employed = total assets - current liabilities
```

Use the alternative only when the cash-adjusted formula is not appropriate. Label the formula.

ROA:

```text
PAT / average total assets * 100
```

Use ROA mainly for banks, NBFCs, insurers, and asset-heavy financial models.

## Debt and Solvency

```text
Gross debt = current borrowings + non-current borrowings + current maturities of long-term debt
Net debt = gross debt - cash and cash equivalents - liquid investments available for debt repayment
Debt-to-equity = gross debt / net worth
Net debt-to-EBITDA = net debt / EBITDA
Interest coverage = EBIT / finance cost
```

For debt-repayment IPOs, compute pre-issue and pro-forma post-repayment leverage when the objects section discloses repayment amount.

If EBITDA is negative, net debt/EBITDA is not meaningful. Use net cash/debt, interest cover, burn, and runway.

For banks and NBFCs, do not penalize debt-to-equity mechanically. Use capital adequacy, GNPA, NNPA, provision coverage, RoA, RoE, and liquidity.

## Cash Conversion

```text
OCF/PAT = cash flow from operations / PAT
Cumulative OCF/PAT = sum(CFO over full years) / sum(PAT over full years)
OCF/EBITDA = cash flow from operations / EBITDA
Free cash flow = cash flow from operations - maintenance capex
FCF/PAT = free cash flow / PAT
```

If maintenance capex is unavailable, use purchase of PPE and intangibles and label the proxy.

Prefer cumulative conversion over a single year. Negative CFO in a profitable business for two or more years is a major quality flag.

## Working Capital

```text
Net working capital = trade receivables + inventory + other current operating assets - trade payables - other current operating liabilities
NWC days = average net working capital / revenue from operations * 365
DSO = average trade receivables / revenue from operations * 365
DIO = average inventory / COGS * 365
DPO = average trade payables / COGS * 365
Cash conversion cycle = DSO + DIO - DPO
```

Use 365 for full years and actual day count for stub periods. If COGS is not separately disclosed, compute DIO/DPO only when a defensible denominator exists; otherwise show NWC days.

For infra/EPC, split receivables, contract assets, unbilled revenue, retention money, mobilisation advances, and payables.

For SaaS or subscription businesses, deferred revenue and customer advances can create negative working capital. Treat this as positive only when retention and service-delivery obligations are credible.
