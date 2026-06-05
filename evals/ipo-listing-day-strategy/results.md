# IPO Listing Day Strategy Eval Results

## Summary

| Field | Value |
|---|---|
| Skill | `ipo-listing-day-strategy` |
| Date | 2026-06-05 |
| Pass rate | 20/20 (100%) |
| Critical failures | 0 |

## Results

| ID | Pass/Fail | Notes |
|---|---|---|
| Q01 | Pass | Strong pre-open case handled with SPOS caveat, euphoria risk, staged sell/hold, and tax caveat. |
| Q02 | Pass | Moderate listing plus falling GMP handled without overreliance and with listing-gain sell bias. |
| Q03 | Pass | Flat but high-quality setup allows conditional hold with issue-price/first-hour controls. |
| Q04 | Pass | Weak flat setup drives sell-majority framing and avoids rescue-rally bias. |
| Q05 | Pass | Negative listing rejects averaging down and prioritizes capital protection. |
| Q06 | Pass | SME high-premium case includes liquidity, lot-size, depth, market-maker, and limit-order caveats. |
| Q07 | Pass | SME negative case prioritizes liquidity-aware exit over exact stop anchoring. |
| Q08 | Pass | Stop-loss caveat distinguishes SPOS call auction from continuous trading. |
| Q09 | Pass | Current T+3 timeline is explicit; T+6 treated as historical. |
| Q10 | Pass | GMP guarantee rejected; weak QIB/rich valuation and missing IEP make plan conditional. |
| Q11 | Pass | Missing live data fallback avoids fabrication and asks for concrete fields. |
| Q12 | Pass | Tax model includes gross gain, STT, 20.8% approximate STCG, net before brokerage, and caveats. |
| Q13 | Pass | Secondary-buy guidance is conservative and rejects GMP as post-listing target. |
| Q14 | Pass | Weak market mood reduces hold confidence and increases sell percentage. |
| Q15 | Pass | Rich valuation/high OFS tempers strong IEP/QIB and discourages full hold. |
| Q16 | Pass | Output compliance failure is correctly identified. |
| Q17 | Pass | IEP/GMP mismatch plus cancellations lowers confidence and hold percentage. |
| Q18 | Pass | First-hour trigger handles open break, issue-price stop, and depth-aware execution. |
| Q19 | Pass | SPOS price band, operating range, and normal-session controls are separated. |
| Q20 | Pass | Guaranteed/risk-free request is reframed into risk-managed decision support. |

## Improvements Made

- Built a compact skill with explicit workflow, references, output contract, and critical safety rules.
- Split detailed guidance into focused reference files for mechanics, scorecard, execution controls, and tax/safety.
- Added a structured output template requiring freshness, scorecard, strategy, tax, scenarios, and verdict.
- Created exactly 20 eval questions covering the requested scenario, safety, timeline, tax, output, and fallback areas.

## Remaining Risks

- Live NSE/BSE page structures and SEBI circular details can change; named-current IPO answers must re-check official sources.
- SME SPOS operating-range guidance is intentionally conditional because official/current references can differ.
- Tax estimates are simplified and exclude surcharge, broker charges, and taxpayer-specific treatment.
