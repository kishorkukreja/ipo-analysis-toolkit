# Source Rules

## Source Hierarchy

1. Official offer documents and filings: DRHP/RHP/prospectus from SEBI, NSE, BSE, issuer, or registrar; anchor allocation filings; post-listing shareholding patterns; corporate announcements.
2. Regulator and exchange rules: SEBI ICDR regulations and circulars, NSE/BSE listing notices, NSE Emerge and BSE SME rules.
3. Valuation and market data: RHP peer table first, then listed peer filings and credible market-data sources.
4. IPO aggregators and media: Chittorgarh, InvestorGain, IPOWatch, financial media, and broker education pages only as secondary context.

## Required Caveats

- GMP is informal, unregulated, source-variable, and not a valuation input.
- Aggregator calendars can lag official exchange updates.
- Subscription snapshots need timestamp and category definitions.
- Post-listing prices, traded value, and shareholding patterns can change daily; current named IPO analysis requires fresh source checks.
- If a primary document cannot be found, continue only with a clearly marked low-confidence analysis or ask for the exact URL.

## Current Defaults

- Indian IPO listing timeline default is T+3 working days. T is issue closing date.
- T+3 is mandatory for public issues opening on or after 2023-12-01.
- SME IPO process changed for issues opening on or after 2025-07-01. Confirm the issue open date before applying process-sensitive SME mechanics.
- Use Rs and Indian units such as crore and lakh.
- Indian fiscal years run April to March.

## Source Log Fields

For each material source, capture:

| Field | Required detail |
|---|---|
| Source | SEBI, NSE, BSE, issuer, registrar, peer data provider, aggregator |
| URL or document | Link or document title |
| Checked at | Date/time in IST |
| Used for | Price, peers, financials, lock-in, liquidity, rule, caveat |
| Reliability | Primary, rule source, peer data, secondary, missing |

