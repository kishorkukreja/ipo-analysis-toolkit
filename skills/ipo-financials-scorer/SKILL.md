---
name: ipo-financials-scorer
description: Build a financial quality scorecard for Indian NSE/BSE mainboard and SME IPOs from DRHP, RHP, prospectus, and exchange disclosures. Use when a user asks to score IPO financials, compare restated financial trends, assess revenue growth, margins, ROE, ROCE, debt, cash conversion, working capital, or produce a Strong/Moderate/Weak financial label without giving an apply/avoid recommendation.
---

# IPO Financials Scorer

Use this skill to turn Indian IPO offer-document financial disclosures into a structured financial scorecard for retail research. The output is decision support, not personalized investment advice.

## Required Inputs

- IPO name.
- Mainboard, NSE Emerge, or BSE SME classification. If unknown, look it up.
- Issue open date when SME process guidance or listing timeline context matters.
- DRHP, RHP, prospectus, exchange filing, or SEBI filing URL if the user has one.

If no offer document is available, search official sources first. If the document still cannot be found, ask for the DRHP/RHP/prospectus URL and provide only a limited fallback using clearly labeled secondary sources.

## Workflow

1. Identify the IPO and classify it as mainboard or SME.
2. Check data freshness and source hierarchy:
   - Prefer SEBI offer-document pages, exchange-hosted offer documents, RHP/prospectus PDFs, and official issuer/BRLM pages.
   - Use draft abridged prospectus only as a navigation aid unless the full offer document is inaccessible.
   - Use broker or aggregator summaries only as fallback, and label confidence as limited.
3. Extract restated financial information:
   - Use restated consolidated financial information first.
   - Use standalone only when no group/consolidation issue exists or the offer document requires it.
   - Keep stub periods separate from full-year scoring.
4. Normalize units and periods:
   - Use Rs crore unless the source is clearer in Rs lakh or Rs million.
   - Treat Indian fiscal years as years ending March 31, for example FY2025 is year ended 2025-03-31.
   - Do not blend stub periods into 3-year CAGR unless annualized and explicitly flagged.
5. Compute the score with the 100-point financial-only model in [scoring-model.md](references/scoring-model.md).
6. Apply sector and SME adjustments from [sector-adjustments.md](references/sector-adjustments.md).
7. Apply caps and critical overrides from [overrides-and-safety.md](references/overrides-and-safety.md).
8. Render the answer using [output-template.md](assets/output-template.md).

## Core Metrics

Always attempt these before scoring:

- Revenue growth, preferably 3-year CAGR across full financial years.
- EBITDA margin and PAT margin trend.
- ROE or RoNW and ROCE; for banks/NBFCs use RoA, RoE, capital adequacy, and asset quality instead.
- Gross debt, net debt, debt-to-equity, net debt/EBITDA, and interest cover.
- CFO/PAT, cumulative CFO/PAT, FCF where capex data supports it.
- Working capital discipline: NWC days, DSO, DIO, DPO, and cash conversion cycle where applicable.
- Disclosure and earnings quality: restatement basis, auditor qualifications, issuer KPIs, one-offs, related-party flows, customer concentration, and contingent liabilities.

Load [metric-formulas.md](references/metric-formulas.md) when you need exact formulas or substitutions.

## Score Labels

- `Strong`: 75-100, unless capped.
- `Moderate`: 55-74, or a stronger raw score capped by manageable risk.
- `Weak`: 30-54, or a moderate raw score capped by serious risk.
- `Avoid-level financial risk`: 0-29, or any critical financial override.

Use `financial_score_label`. Do not output `Apply`, `Avoid`, `Subscribe`, or guaranteed listing-gain language. Valuation, GMP, subscription, allotment odds, and final application verdicts belong to other IPO skills.

## SME and Timeline Rules

- State whether the IPO is mainboard, NSE Emerge, or BSE SME.
- Current Indian IPO listing timeline default is T+3 working days, where T is issue close date. T+3 is mandatory for public issues opening on or after 2023-12-01. Treat T+6 as historical unless analyzing an older issue.
- For SME IPOs, use stricter confidence and score caps when disclosure is thin, customer concentration is high, CFO quality is weak, related-party activity is material, or scale is very small.
- For SME IPO process details opening on or after 2025-07-01, verify current exchange/SEBI rules before giving action-specific process guidance.

## Missing Data Behavior

- Do not invent financial line items, dates, KPIs, or formulas.
- If a metric cannot be computed, mark it `not available` or `not meaningful`, explain why, and score using the nearest defensible proxy.
- If only an abridged prospectus or secondary summary is available, set confidence to `Low` or `Medium-Low` and label the source limitation.
- If PAT endpoints are negative or near zero, do not compute PAT CAGR; use loss-making rules and trend quality.

## Safety

- Frame outputs as financial research support.
- Do not guarantee returns, allotment, listing gains, GMP reliability, or a final investment outcome.
- Do not give personalized investment advice. Use score labels, risk implications, and caveats.
- Mention valuation only as context found in the offer document and hand it off to `ipo-peer-comparison` or `ipo-apply-advisor`.
