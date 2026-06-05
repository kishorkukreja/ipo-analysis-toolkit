# Agent Instructions

This plugin contains Indian IPO skills only. Do not add non-IPO trading or investment skills here, and do not add IPO skills back into `finance-trading-skills/skills`.

## Shared IPO Defaults

- Current default IPO listing timeline: T+3.
- Treat old T+6 references as historical unless the user is asking about an older issue.
- SME IPO rules changed for issues opening on or after 2025-07-01. Always ask or infer the issue open date before applying process-specific SME guidance.
- Distinguish mainboard from SME on risk, lot size, liquidity, application mechanics, and listing platform.
- GMP is informal, unregulated, and source-variable. Use it only with caveats and never as the sole basis for an apply/avoid verdict.

## Source Hierarchy

1. SEBI circulars, SEBI offer-document pages, NSE/BSE exchange pages, registrar pages.
2. DRHP/RHP/prospectus PDFs and official issuer filings.
3. Reputable IPO aggregators and broker education pages, with clear caveats.
4. News and social/grey-market commentary only as secondary context.

When live data is missing, state what was unavailable, provide a safe fallback, and ask for the specific URL or document needed.

