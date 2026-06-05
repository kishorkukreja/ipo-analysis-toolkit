# Source and Peer Selection

## Source Hierarchy

Use official and issuer-controlled sources first:

1. DRHP, RHP, prospectus, price-band ad, and basis-of-issue-price section from SEBI, NSE, BSE, issuer, registrar, or BRLM pages.
2. Restated financial statements and KPI or WACA disclosures from the offer document.
3. NSE/BSE company pages, filings, exchange disclosures, and NSE Indices factsheets for listed peers.
4. Current peer market data from available market-data tools.
5. Secondary fills: Screener, Trendlyne, TickerTape, Moneycontrol, StockEdge, Chittorgarh, InvestorGain, IPOWatch, broker notes, equity research, and Damodaran sector data.

Rules:

- Prefer DRHP/RHP values over media summaries.
- Prefer consolidated numbers when the issuer reports consolidated financials.
- Flag standalone-vs-consolidated mismatches.
- Do not mix FY latest, TTM, interim annualized, and forward peer data silently.
- Do not use GMP, oversubscription, anchor demand, or listing hype as valuation proof.

## Define the Real Business

Avoid broad sector labels. Build the peer universe around revenue economics.

Useful business descriptions:

- Indian IT services with BFSI/US client exposure.
- Specialty chemicals contract manufacturer with export mix.
- Housing finance NBFC focused on self-employed borrowers.
- Asset-light B2B SaaS with subscription ARR.
- EMS manufacturer for mobile and consumer electronics.
- D2C retailer with online/offline channel mix.

Infer this from revenue segments, geography, customer concentration, cost structure, regulation, capital intensity, and margin drivers.

## Indian Peer Priority

Use Indian listed peers for the primary verdict whenever a meaningful Indian analogue exists. Search in this order:

1. Direct competitors named in the DRHP/RHP.
2. NSE/BSE listed companies in the same sub-sector.
3. NSE Indices factsheet constituents for sector context.
4. Screener, Trendlyne, TickerTape, and broker peer pages.
5. Adjacent Indian listed proxies with similar economics.
6. Global peers only when Indian peers are absent or misleading.

Global comps are fallback evidence. State market, currency, accounting, size, liquidity, growth, and regulatory caveats. Apply an explicit adjustment rather than hiding an "India discount".

## Comparability Filters

Score each peer before including it in the median:

| Dimension | Preferred threshold | Why it matters |
|---|---:|---|
| Revenue size | 0.3x to 3.0x issuer revenue | Large-cap multiples can overstate small IPO value. |
| EBITDA margin | within +/- 10 percentage points | P/S and EV/Sales need margin comparability. |
| Revenue growth | within +/- 15 percentage points | Growth premiums need evidence. |
| ROE/ROCE/ROA | same quality band | Return quality supports or rejects premiums. |
| Geography | similar domestic/export exposure | Export, currency, and regulation change multiples. |
| Customer type | B2B, B2C, government, tender, platform | Revenue stability and receivable risk differ. |
| Capital intensity | asset-light vs asset-heavy | Book value and EV multiples behave differently. |
| Leverage | similar net debt/EBITDA | Equity multiples can mislead when debt differs. |
| Liquidity | adequate trading value | Illiquid prices can be stale. |

Peer count confidence:

- High: at least 4 good Indian peers.
- Medium: 3 peers or a mostly direct set with minor mismatches.
- Low: fewer than 3 direct peers, only global comps, SME peers with poor liquidity, major one-offs, or poor disclosure.

## Peer Labels

Label every company:

- `Direct Indian peer`
- `Adjacent Indian proxy`
- `Large-cap benchmark`
- `Small-cap/SME peer`
- `Global direct peer`
- `Global proxy`
- `Excluded DRHP peer`

Excluded peers need a one-sentence reason, such as scale mismatch, business-model mismatch, negative earnings, stale data, low liquidity, one-off EPS, or accounting-period mismatch.

## DRHP Peer Table Audit

Treat the issuer's peer table as evidence, not truth. Test:

| Test | Pass/Fail | Failure pattern |
|---|---|---|
| Same sub-sector | | Broad industry peer used to inflate multiples. |
| Similar scale | | Mature large caps used for small issuer. |
| Similar margins/growth | | Weak issuer compared with premium-quality peers. |
| Similar capital intensity | | Distributor compared with manufacturer. |
| Similar geography/customer type | | Export, domestic, regulated, and tender exposure ignored. |
| Same accounting basis | | Consolidated issuer mixed with standalone peers. |
| Same period | | FY, TTM, and forward multiples mixed silently. |
| Enough peers | | One-peer table presented as reliable. |
| Obvious peers included | | Competitors omitted without explanation. |
| Median not just average | | Outlier average used to support price. |

Audit labels:

- `DRHP peer set looks reasonable`
- `DRHP peer set is usable but incomplete`
- `DRHP peer set is broad/weak`
- `DRHP peer set appears cherry-picked`
- `No meaningful DRHP peer comparison`
