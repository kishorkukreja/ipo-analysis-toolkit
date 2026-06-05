---
name: ipo-scenario-simulator
description: Use when a user wants bull/base/bear post-listing scenarios, 6-month or 12-month price ranges, valuation rerating risk, or lock-in supply-overhang analysis for an Indian mainboard or SME IPO after allotment or listing.
---

# IPO Scenario Simulator

Model what can happen after an Indian IPO lists. This is scenario research, not an apply/avoid decision and not personal financial advice.

## Use This For

- 6-month and 12-month bull/base/bear price ranges after listing.
- Current holder, allottee, or secondary buyer risk/reward framing.
- Valuation re-rating or de-rating from IPO/current valuation to peer multiples.
- Anchor, pre-IPO, promoter, PE/VC, ESOP, or other lock-in expiry pressure.
- SME IPO post-listing scenarios where liquidity, lot size, market-maker quality, and shallow order books matter.

Do not use this skill for application advice, live GMP tracking, or listing-session trading tactics.

## Required Sources

For named IPOs, fetch current information. If the user provides a DRHP/RHP/prospectus, exchange filing, registrar page, or listed symbol, use that first. If a required official document cannot be found, state the gap and ask for the exact URL instead of inventing figures.

Use this hierarchy:

1. Official offer documents, SEBI pages, NSE/BSE issue pages, anchor filings, post-listing shareholding, corporate announcements, and registrar pages.
2. SEBI ICDR regulations/circulars and NSE/BSE SME/mainboard rule pages.
3. RHP peer table, listed peer filings, exchange data, and credible market-data sources.
4. IPO aggregators and media only as secondary context. GMP is informal, unregulated, and not a valuation input.

Record source date/time checked in IST and mark every estimate as sourced, calculated, or heuristic.

## Minimum Inputs

Collect or clearly mark missing:

- Company name, symbol, classification: mainboard, NSE Emerge, or BSE SME.
- Issue open date, allotment date, listing date, issue price, listing price, listing-day close, current price.
- Issue structure: fresh issue, OFS, post-issue shares, market cap, EV, free float.
- Subscription by category, anchor allocation, anchor names, and post-listing institutional ownership.
- Financial metric for valuation: EPS, EBITDA, book value, revenue, AUM, embedded value, ARR, or sector KPI.
- Peer median multiple and current company multiple.
- Lock-in table for anchor, pre-IPO, promoter, promoter excess, PE/VC, ESOP, and special shareholder arrangements.
- 60-trading-day average volume/value when available. For SME, also collect market lot size, daily traded lots, spread/circuit behavior, and market-maker context.

Ask only for user-specific inputs if needed: buy price, quantity, time horizon, risk tolerance, or tax-adjusted exit math.

## Workflow

1. Classify the IPO as mainboard or SME and confirm the issue open date. Current default listing timeline is T+3 working days, where T is issue close date. For SME issues opening on or after 2025-07-01, verify process-specific mechanics before applying them.
2. Build the data sheet from official sources first. If peer, liquidity, or lock-in data is missing, continue with a low-confidence scenario and state exactly what is missing.
3. Select the valuation metric from the issuer type:
   - Profitable operating company: EPS * P/E, cross-check EV/EBITDA or P/S.
   - Manufacturing, hospitals, logistics, capital goods: EBITDA * EV/EBITDA, cross-check P/E and debt.
   - Bank/NBFC/HFC/MFI: book value * P/B, cross-check ROA, ROE, credit cost.
   - Insurance: embedded value * P/EV, VNB margin, APE growth.
   - AMC/wealth: AUM or EBITDA multiple, cross-check P/E.
   - SaaS/platform/loss-making: revenue, ARR, gross profit, or contribution margin multiple. Do not compute fake P/E.
   - SME: use the sector metric with explicit liquidity and credibility discounts.
4. Forecast the 6-month and 12-month metric. Use guidance or estimates if available. Otherwise infer from RHP history, interim results, sector trend, margins, order book/AUM/ARR, and cash conversion. Haircut growth for customer concentration, acquisition-led growth, weak OCF, working-capital stress, delayed capex, or reversed sector tailwinds.
5. Choose bull/base/bear multiples from peer median and current/IPO valuation. Explain re-rating or de-rating using growth, margins, ROCE, scarcity, governance, disclosure quality, sector trend, liquidity, and supply overhang.
6. Build the unlock calendar from allotment date unless the offer document says otherwise:
   - Anchor first 50%: allotment date + 30 days.
   - Anchor remaining 50%: allotment date + 90 days.
   - Non-promoter pre-issue capital: generally allotment date + 6 months.
   - Promoter holding above minimum promoter contribution: generally allotment date + 6 months.
   - Minimum promoter contribution: generally allotment date + 18 months, with longer periods possible in specified capex-heavy cases.
   - Pledged/frozen locked shares: check 2026 non-transferability disclosures; do not treat them as freely sellable just because normal lock-in marking is unclear.
7. Score supply overhang:
   - Expected sellable shares = unlock shares * holder sell probability.
   - Overhang ratio = expected sellable shares / 60-trading-day average daily traded volume.
   - Low: <20 trading days of volume; Moderate: 20-60; High: 60-120; Extreme: >120.
   - For SME, also calculate expected sell lots / daily traded lots.
8. Convert scenarios to price and return ranges:
   - Fundamental value target = projected metric * scenario multiple.
   - Scenario target = fundamental value target - supply-overhang discount + event/catalyst adjustment.
   - Show ranges, not exact targets. Always show downside.
9. Assign heuristic probabilities in 5% increments that sum to 100%. Label confidence High/Medium/Low. Reduce confidence when current price, peers, lock-ins, liquidity, or post-listing financials are missing.
10. Finish with the output template in `assets/output-template.md`, including verdict block, source log, caveats, and no guaranteed outcome language.

## Probability Defaults

Start here, then adjust for quality, valuation, listing pop, QIB/anchor quality, execution, sector mood, liquidity, and supply pressure.

| Setup | Bull | Base | Bear |
|---|---:|---:|---:|
| High-quality mainboard, fair valuation, strong QIB | 30% | 50% | 20% |
| Average mainboard, fair/rich valuation | 20% | 50% | 30% |
| Richly priced or weak QIB mainboard | 15% | 40% | 45% |
| High-quality SME with strong liquidity | 25% | 45% | 30% |
| Typical SME | 15% | 40% | 45% |
| Weak SME or very high listing pop | 10% | 30% | 60% |

## Required Caveats

- Scenario ranges are conditional: "If these assumptions are true, the likely range is..."
- Probabilities are heuristic bands, not statistical certainties.
- No scenario may guarantee returns, allotment, exit liquidity, or listing outcomes.
- GMP is not official, not regulated, and not sufficient for scenario valuation.
- Mainboard and SME outputs must differ on liquidity, lot-size risk, depth, and confidence.
- Use absolute dates for unlocks and catalysts; avoid relative wording like "next month."

## References

- `references/source-rules.md`
- `references/scenario-method.md`
- `references/lock-in-supply-overhang.md`
- `references/sme-post-listing.md`
- Shared references in `skills/shared/references/`
