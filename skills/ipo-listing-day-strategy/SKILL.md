---
name: ipo-listing-day-strategy
description: Build an Indian IPO listing-day sell/hold plan for retail allottees using SPOS/pre-open signals, subscription quality, GMP context, valuation, market mood, SME liquidity, tax drag, and risk controls.
metadata:
  short-description: Indian IPO listing-day action plan
---

# IPO Listing Day Strategy

Use this skill when the user asks what to do with an Indian IPO allotment on listing day, how to interpret pre-open/listing signals, whether to sell or hold after listing, or whether to buy a newly listed IPO. It covers NSE/BSE mainboard, NSE Emerge, and BSE SME IPOs.

## First Principles

- Frame the answer as decision support, not personalized financial advice.
- Current default Indian IPO listing timeline is T+3 working days from issue close. Treat T+6 as historical unless an older issue explicitly used it.
- For every named live IPO, web-check current data if browsing is available. Prefer NSE, BSE, SEBI, issuer, registrar, and offer-document sources before IPO aggregators.
- Always distinguish mainboard from SME before advising action. If classification is missing, mark it as a required lookup and give only a conditional plan.
- Treat GMP as informal, unregulated sentiment. Never use GMP alone to justify sell, hold, or buy.
- The default user is a retail allottee planning exit/hold. Discuss secondary buying only if asked, and keep it conservative.

## Required References

Read only what is needed:

- `references/listing-day-mechanics.md` for SPOS, IEP, price controls, and T+3 timing.
- `references/signal-scorecard.md` for IEP/GMP/subscription/valuation/market interpretation.
- `references/execution-risk-controls.md` for sell/hold matrix, stop-loss caveats, SME liquidity, and secondary-buy rules.
- `references/tax-and-safety.md` for STCG/STT estimates and compliance caveats.
- `../shared/references/india_ipo_data_sources.md` and `../shared/references/sme_vs_mainboard.md` for shared source and SME framing.
- `assets/output-template.md` for the required answer structure.

## Workflow

1. Collect inputs and source status.
   - Company, symbol, exchange, mainboard/SME, issue price, lot size, allotted quantity, issue size, listing date, and user intent.
   - If the user gives a named current IPO, check live/most recent data and timestamp it in IST. If live data cannot be checked, say so and ask for the missing link, screenshot, or values.
   - If the user only asks a general scenario, use a hypothetical framework and label it as such.

2. Check listing mechanics.
   - Indian IPO listing-day price discovery uses the Special Pre-Open Session from 9:00 AM to 10:00 AM, not the normal 9:15 AM open.
   - Order entry/modification/cancellation runs 9:00-9:45 AM with random closure in the last 10 minutes; matching runs 9:45-9:55 AM; continuous trading starts at 10:00 AM.
   - IEP is the indicative equilibrium price. Interpret it with indicative quantity, buy/sell depth, cancellations, and timing. Early IEP can be unreliable.
   - Do not state a fixed SME listing circuit without checking current exchange controls. Distinguish SPOS operating ranges from first-day normal-session price bands.

3. Build the signal scorecard.
   - IEP premium/discount versus issue price: strong `>= +25%`, positive `+10% to +25%`, flat `within +/-3%`, weak below issue price.
   - Compare IEP with latest GMP-implied price. If IEP is materially below GMP, reduce confidence and hold percentage.
   - Evaluate QIB, NII, retail, and overall subscription separately. Give QIB and anchor quality more weight than headline overall subscription.
   - Add valuation/fundamentals and market mood. A rich valuation or weak Nifty/sector morning increases sell bias.
   - For SME, add an explicit liquidity warning even when the premium is high.

4. Convert signals into an action plan.
   - Use staged action: recommended action, sell percentage, hold percentage, stop-loss level, first-hour trigger, and confidence.
   - Strong premium: default partial profit booking; above 40% add euphoria risk.
   - Moderate premium: balance tax drag, user intent, valuation, and QIB quality.
   - Flat listing: hold only when QIB/anchor quality, valuation, depth, and first-hour behavior support it.
   - Negative listing: prioritize capital protection; do not average down on listing day.
   - SME listing: sell more aggressively when liquidity is thin or premium is GMP-driven.

5. Add risk, tax, and fallback caveats.
   - Stop-loss orders do not work the same way in SPOS; use limit-order planning in pre-open and normal-session stops only after continuous trading starts.
   - If exact prices are unavailable, use conditional stops such as issue-price breach, first-hour low, open break, or liquidity window.
   - For listing-day sale of listed equity where section 111A/STT conditions apply, use 20% STCG plus 4% cess as an approximate 20.8% tax drag, excluding surcharge and broker-specific costs.
   - State that tax depends on taxpayer facts and is not tax advice.

## Output Contract

Use the template in `assets/output-template.md`. Every answer should include:

- Data freshness and missing-data warnings.
- Listing setup.
- Live/pre-open signal or hypothetical scenario label.
- Input scorecard.
- Strategy with sell/hold percentages and stop/trigger.
- Net outcome or tax caveat.
- Scenario table.
- Verdict table with action, confidence, sell now, hold, stop-loss, listing signal, and main risk.

## Critical Safety Rules

- Never say listing gain, GMP, IEP, or exit price is guaranteed.
- Never recommend averaging down on listing day.
- Never present GMP as official data or as a post-listing buy target.
- Never ignore SME liquidity, lot size, or market-maker limitations.
- Never advise a market order in a thin SME listing; prefer limit orders and liquidity-aware execution.
- Do not fabricate live data. If data is missing, give a conditional framework and list exactly what is needed.
