# SME Post-Listing Treatment

SME IPO scenarios need a separate liquidity layer. A displayed price may not be an executable exit price for a retail holder because market lots, shallow depth, spread, circuit locks, and market-maker behavior can dominate fundamentals.

## Required SME Fields

- Platform: NSE Emerge or BSE SME.
- Issue open date, especially whether it is on or after 2025-07-01.
- Market lot size and retail lot value.
- Average daily traded value.
- Average daily traded shares and lots.
- Bid/ask spread, circuit behavior, and frequency of no-trade or low-depth sessions.
- Market maker and quote-depth context where available.
- Whether odd-lot exit would require a separate odd-lot matching mechanism.

## SME Liquidity Score

| Condition | Interpretation |
|---|---|
| Average daily traded value > Rs 5 crore | Better liquidity, still verify depth |
| Average daily traded value Rs 1-5 crore | Moderate liquidity |
| Average daily traded value < Rs 1 crore | Low liquidity, apply discount |
| Average daily traded lots < 20 | High exit-risk warning |
| Bid/ask spread > 3% | Liquidity discount |
| Frequent circuit locks | High exit-risk warning |
| Quote depth only near minimum market-maker obligation | Liquidity discount |

## Probability Adjustments

- Reduce bull probability by 5-10 percentage points unless liquidity remains strong after 30 days.
- Increase bear probability by 10-20 percentage points if the SME had a large listing pop.
- Apply a 10-35% liquidity discount when traded value is low.
- Use market-lot-adjusted overhang ratio, not only share-volume ratio.

## Required Caveat

Include this meaning in every SME scenario:

```markdown
SME liquidity caveat: Price targets are lower confidence because market lot size, thin order book, market-maker dependency, and circuit behavior can make exits difficult even when the displayed price looks attractive.
```

