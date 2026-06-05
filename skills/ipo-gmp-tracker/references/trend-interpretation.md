# Trend Interpretation

## Trend Sequence

Build a day-wise GMP sequence when data is available:

1. Pre-open GMP.
2. Day 1 open or close GMP.
3. Day 2 close GMP.
4. Day 3 or final subscription day GMP.
5. Post-close GMP.
6. Allotment-day GMP.
7. Final 24-48 hour GMP.
8. Listing-morning GMP, if available.

If a user gives only the latest value, do not invent a trend. Mark trend as unknown and explain which historical rows are needed.

## Classifications

| Trend | Pattern | Interpretation |
|---|---|---|
| Rising steadily | GMP increases across days without sharp reversals | Demand building; more useful if subscription also improves |
| Rising sharply | Large Day 2/Day 3 jump | Strong momentum, but verify QIB/NII support |
| Flat positive | GMP remains positive within a narrow range | Stable sentiment, especially useful near listing |
| Flat zero | GMP stays near zero | Weak listing-gain signal; focus on fundamentals |
| Falling from high | Early high GMP compresses into close or listing | Hype fading; caution |
| Volatile | Wide day-wise swings | Low confidence |
| Divergent | Sources disagree materially | Low confidence until resolved |
| Unknown | Too few dated rows | Do not infer direction |

## Numeric Flags

```text
trend_delta_pct = (latest_gmp - first_valid_gmp) / issue_price * 100
trend_ratio = latest_gmp / first_valid_gmp, when first_valid_gmp > 0
source_spread_pct_of_issue = (max_source_gmp - min_source_gmp) / issue_price * 100
```

Use these thresholds:

- Source spread up to 3% of issue price: consistent.
- Source spread from 3% to 8%: moderate disagreement.
- Source spread above 8%: major disagreement.
- Latest GMP down more than 50% from peak: hype fading.
- Latest GMP up more than 50% from first valid GMP: momentum rising; check subscription quality.
- GMP unchanged for 3+ days at an exact round number: possible stale or held quote.

## SME Trend Caution

For SME IPOs, trend interpretation starts more conservative because informal GMP can be easier to distort. Always mention:

- Larger minimum application and trading-lot exposure.
- Lower liquidity and wider spread risk.
- Market-maker obligations do not guarantee an easy exit.
- High GMP can be hard to realize if the stock hits circuit limits or lacks buyers.
