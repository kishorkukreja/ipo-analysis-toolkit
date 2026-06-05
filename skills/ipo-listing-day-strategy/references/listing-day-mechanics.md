# Listing Day Mechanics

## Current Timeline

- Default Indian IPO listing timeline is T+3 working days from issue close for public issues opening on or after 2023-12-01.
- Use `YYYY-MM-DD` dates when timeline affects the answer.
- Treat T+6 as historical unless an old offer document or older issue date applies.

## Special Pre-Open Session

IPO and SME IPO listing-day price discovery occurs through the Special Pre-Open Session (SPOS), not the normal 9:15 AM open.

| Time | Phase | Interpretation |
|---|---|---|
| 9:00-9:45 AM | Order entry, modification, cancellation; random closure in last 10 minutes | Watch IEP trend, indicative quantity, buy/sell depth, and cancellations. Early readings are weaker. |
| 9:45-9:55 AM | Matching and trade confirmation | Final opening price is determined. No normal stop-loss behavior applies. |
| 9:55-10:00 AM | Buffer | Prepare normal-session order plan. |
| 10:00 AM onward | Continuous trading | Execute staged sell/hold plan and monitor first 15-60 minutes. |

## IEP

IEP is the indicative equilibrium price from the auction book. It is a signal, not a guaranteed execution price before final matching.

Use these supporting fields when available:

- Indicative equilibrium quantity.
- Indicative value.
- Total buy/sell depth.
- Cancelled order quantity.
- Timing of changes, especially after 9:25 AM and near random closure.

Label IEP signal strength as `Strong`, `Moderate`, `Weak`, or `Unreliable`.

## Price Controls

Keep these concepts separate:

- SPOS price band: official descriptions say no normal price band in the auction.
- SPOS operating range: exchanges can use operating ranges or price-freeze controls to filter erroneous orders. Check current NSE/BSE guidance on listing morning, especially for SME.
- Normal-session first-day controls: exchange/SEBI rules may apply bands from the discovered equilibrium price or issue price depending on issue size and price discovery.

Do not give a hardcoded SME lower operating range as current trading advice because official/current descriptions can differ. Say to check current exchange operating range on listing morning.

## Preferred Sources

- NSE SPOS and new listing pages.
- BSE SPOS and public issue/listing pages.
- SEBI trading master circulars and current circulars.
- Exchange listing notices for group/series and special conditions.
