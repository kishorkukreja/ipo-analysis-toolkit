# Signal Scorecard

## Source Priority

1. Official exchange/regulator pages for live mechanics and official listing data.
2. Offer document, issuer filings, anchor disclosure, and exchange subscription data.
3. IPO aggregators for GMP, historical performance, and cross-checks.

If live data is missing, do not invent it. State the missing fields and provide a conditional plan.

## IEP Bands

| IEP vs issue price | Signal | Action bias |
|---|---|---|
| `>= +25%` | Strong | Book partial profit; hold only if QIB/valuation/depth support follow-through. |
| `+10% to +25%` | Positive/moderate | Sell partial; hold residual with first-hour trigger. |
| `+5% to +10%` | Modest | Sell more if user wanted listing gain or valuation is rich. |
| Within `+/-3%` | Flat | Hold only with strong QIB, fair valuation, and decent depth. |
| Below issue price | Weak | Prioritize exit discipline and capital protection. |

For `>= +40%`, add an euphoria-risk warning even when the business is good.

## IEP Quality

- Stable/rising IEP after 9:25 AM is stronger than an early spike.
- High IEP with shallow indicative quantity is fragile.
- Late IEP drop plus cancelled buy orders is a warning.
- Heavy sell depth near IEP can cap first-hour upside.
- SME IEP is noisier because depth is thinner and lot sizes are larger.

## GMP Context

Display:

- Latest GMP in INR and percentage.
- Implied listing price = issue price + GMP.
- Trend over recent days: rising, flat, falling, collapsed, or negative.
- Reliability: `Low` by default; `Moderate` only when multiple sources converge and SPOS confirms it.

Interpretation:

- IEP materially above GMP-implied price: official order book is stronger than grey-market sentiment.
- IEP in line with GMP: execute pre-planned staged action.
- IEP materially below GMP: GMP may have overstated demand; reduce hold percentage.
- Negative GMP plus weak IEP: high-risk setup; prioritize exit.

Never use GMP as a reason to buy after listing.

## Subscription Quality

| Pattern | Interpretation | Action bias |
|---|---|---|
| QIB > 10x and overall > 50x | Strong institutional demand | Hold partial if valuation and depth support it; sell into very high pop. |
| QIB 3-10x with strong retail/NII | Positive but less durable | Sell 40-70% depending on IEP. |
| QIB < 1x or weak anchor book | Poor institutional support | Sell aggressively on flat/negative listings. |
| NII extremely high but QIB moderate | Leverage-driven demand possible | Sell into pop; avoid chasing. |
| Retail high, QIB low | Sentiment-driven | Reduce hold percentage. |

## Valuation And Market Mood

- Fair/discounted valuation, strong growth, and cash conversion support holding a residual position.
- Rich valuation, weak cash flow, high OFS, or weak growth increase sell bias.
- Nifty down more than 1% or sector down more than 1.5% on listing morning should reduce hold confidence.
- Bullish market breadth makes partial hold more defensible, not risk-free.
