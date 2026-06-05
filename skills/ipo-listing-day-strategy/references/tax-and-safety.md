# Tax And Safety

## Listing-Day Tax Model

For Indian listed equity sold within 12 months where STT conditions apply, section 111A short-term capital gains treatment generally applies.

Use this default only as an estimate:

- STCG base rate: 20% for transfers on or after 2024-07-23.
- Health and education cess: 4%.
- Approx effective STCG rate: 20.8%.
- STT on delivery-based sale: 0.1% of sale value, payable by seller.
- Exclude surcharge, brokerage, exchange charges, SEBI fees, stamp duty, GST, set-offs, and taxpayer-specific issues unless the user provides details.

Formula:

```text
Gross gain = (sell price - issue price) * shares
STT on sale = sell price * shares * 0.001
Approx STCG tax = max(gross gain, 0) * 0.208
Approx net gain before brokerage = gross gain - STT on sale - approx STCG tax
```

If there is a loss, do not subtract STCG tax. Say loss set-off treatment depends on tax facts.

## Safety Language

Use plain language:

- "This is a listing-day framework, not personalized investment advice."
- "Actual tax depends on residential status, income level, surcharge, set-offs, STT eligibility, and filing position."
- "GMP is informal and unregulated."
- "IEP is a live auction signal, not a guaranteed final price until matching."

Avoid:

- "Sure shot"
- "Guaranteed listing gain"
- "Risk-free"
- "Average down on listing day"
- "Buy because GMP is high"
- "Use market order" for thin SME listings

## Missing Live Data Fallback

When current web data is unavailable:

1. State the unavailable fields.
2. Say the plan is conditional, not final.
3. Ask for a current NSE/BSE page, broker screenshot, or values for IEP, IEQ, depth, cancellations, GMP, subscription, and issue price.
4. Provide scenario branches for strong, moderate, flat, and negative listing instead of pretending to know live data.
