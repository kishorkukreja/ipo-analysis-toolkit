---
name: ipo-peer-comparison
description: Compares an Indian IPO's valuation against listed peers using sector-appropriate multiples, peer-set audits, and premium/discount logic. Use when a user asks whether an NSE/BSE mainboard or SME IPO is cheap, expensive, fairly priced, overvalued, undervalued, or comparable with listed peers.
---

# IPO Peer Comparison

## Purpose

Use this skill to judge whether an Indian IPO's pricing is reasonable versus already-listed alternatives. Do not merely repeat the issuer's DRHP/RHP peer table; use it as evidence, then independently test peer fit, metric fit, and valuation support.

## Required Sources

1. If the user supplies a DRHP/RHP/prospectus URL, use it first.
2. Otherwise search official SEBI, NSE, BSE, issuer, registrar, or BRLM pages for the offer document and price band.
3. Use NSE/BSE pages, exchange filings, NSE Indices, and current listed-company data for peers.
4. Use Screener, Trendlyne, TickerTape, Moneycontrol, Chittorgarh, InvestorGain, IPOWatch, broker notes, or Damodaran only as secondary or fallback sources.
5. Read shared source guidance when needed: `skills/shared/references/india_ipo_data_sources.md` and `skills/shared/references/sme_vs_mainboard.md`.

Always state data freshness, source date, and whether peer multiples are current, FY latest, TTM, forward, consolidated, or standalone.

## Workflow

1. Classify the IPO as mainboard, NSE Emerge, or BSE SME. If unknown, look it up; do not assume.
2. Identify issue context: price band or issue price, upper-band market cap, enterprise value if possible, fresh issue/OFS split, objects of issue, and current default listing timeline of T+3 from issue close where relevant.
3. Define the real business model from revenue segments, geography, customers, margin structure, capital intensity, regulation, and concentration.
4. Extract the DRHP/RHP peer table and audit it for sub-sector fit, revenue scale, margin/growth comparability, accounting basis, period alignment, liquidity, and omitted obvious peers.
5. Build the independent peer set. Prefer 4-6 direct Indian listed peers; accept 3; label weaker sets and global fallback as low confidence.
6. Pick the primary multiple by business model: P/E for profitable stable businesses, P/B for lenders and asset-heavy financials, EV/EBITDA for operating businesses with leverage differences, P/S or EV/Sales for loss-making or new-age issuers, P/EV for life insurers, EV/AUM for AMCs, and NAV premium/discount for real estate or asset pools.
7. Compute premium/discount: `(IPO multiple / peer median multiple) - 1`. Use median as headline, show range, and avoid fake ratios when EPS or EBITDA is negative.
8. Adjust the interpretation for growth, margins, returns, leverage, cash conversion, size, liquidity, issue structure, SME status, one-offs, and source quality.
9. Produce a retail-facing valuation verdict: `Undervalued`, `Fairly priced`, `Expensive but justified`, `Overvalued`, or `Speculative / low confidence`.

## Output Rules

Use `assets/output-template.md`. Required sections are Verdict Snapshot, Company and Issue Context, Peer Set Construction, DRHP Peer Table Audit, Valuation Comparison, Business Quality Benchmark, Premium/Discount Explanation, SME/Mainboard Notes, Retail Investor Interpretation, Source Log, and Caveats.

For SME IPOs, include a specific liquidity caveat covering lot size, thin float, market-maker dependence, impact cost, and lower institutional participation. If the issue opens on or after 2025-07-01 and process guidance affects the answer, verify the issue-open date before applying SME process assumptions.

## Safety Boundary

Provide research support, not personalized financial advice. Do not guarantee allotment, listing gains, returns, or GMP reliability. Do not use GMP, oversubscription, anchor demand, or social commentary as proof of valuation. If data is missing, say what is unavailable and lower confidence rather than inventing a median or verdict.

## References

- `references/source-and-peer-selection.md`
- `references/valuation-methodology.md`
- `references/sme-and-special-cases.md`
- `assets/output-template.md`
