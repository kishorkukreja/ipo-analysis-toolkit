# Source And Safety Rules

## Source Hierarchy

Tier 1:

- DRHP/RHP/prospectus from SEBI, NSE, BSE, issuer, BRLM, or registrar.
- SEBI ICDR regulations, circulars, and investor education pages.
- NSE/BSE subscription data, anchor disclosures, listing notices, basis of allotment.
- Registrar allotment and issue pages.

Tier 2:

- Chittorgarh IPO pages for timetables, subscription summaries, GMP, and listing history.
- InvestorGain for GMP trend, kostak, and subject-to-sauda context.
- IPOWatch for SME cross-checks.
- Broker IPO notes for valuation/business summary, never as the only source.

Tier 3:

- Reputable business press, analyst notes, Screener, Trendlyne, TickerTape, Moneycontrol, and similar peer-data sources.

If Tier 1 and Tier 2 conflict, Tier 1 wins. If GMP conflicts with fundamentals, fundamentals win for long-term view and GMP only affects listing-gain view.

## Required Caveats

- GMP is unofficial, unregulated, informal, and can change rapidly. It is not a guaranteed listing-price signal.
- Subscription snapshots need a timestamp and category definitions. Do not call subscription final unless the source timestamp confirms it.
- Aggregator IPO calendars can lag official exchange updates.
- Broker notes can be useful but may use stale peer data or optimistic assumptions.
- SME disclosures and liquidity can be thinner than mainboard IPOs.
- T+3 is the current default listing timeline; T+6 is historical unless the specific issue proves otherwise.

## Bias Check

If the user is leaning Apply, actively test:

- Whether GMP/subscription is masking poor financials.
- Whether QIB demand is weak or absent.
- Whether valuation already prices in growth.
- Whether any red flag should override listing hype.

If the user is leaning Avoid, actively test:

- Whether weak GMP is masking strong long-term fundamentals.
- Whether QIB/anchor quality is better than retail sentiment suggests.
- Whether valuation is fair enough for a hold.

In the final verdict table, set `Bias adjusted` to exactly `Yes` when a user bias was explicitly tested, otherwise exactly `No`. Put the reason in `Bias Check Result`, not inside the verdict field.

## Safety Boundary

Allowed:

- Structured decision support.
- Scenario analysis.
- Category, capital, cut-off, and risk framing.
- Clear Apply/Avoid/Neutral research verdicts when evidence supports them.

Not allowed:

- Guaranteed allotment, listing gain, or investment return.
- Personalized advice based on undisclosed financial circumstances.
- Instructions to use multiple PANs/accounts to game allotment.
- Recommendations to deploy more capital solely because HNI might improve odds.
- Treating GMP as official or sufficient.

Use phrasing such as `For a retail research decision...` and `This is not a guarantee of returns or allotment.`
