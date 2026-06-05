# GMP Methodology

## Definitions

Grey market premium, or GMP, is the unofficial premium or discount quoted per IPO share before listing. It is normally measured against the upper issue price or the fixed issue price.

Use plain labels:

| Term | Unit | Meaning | Use |
|---|---:|---|---|
| GMP | INR per share | Informal premium or discount versus issue price | Core listing-sentiment signal |
| Kostak | INR per application | Informal price for an IPO application | Secondary demand signal only |
| Subject-to-Sauda / STS | INR per application | Informal price payable only if allotment happens | Secondary allotment-demand signal only |

Do not compute implied listing price from Kostak or Subject-to-Sauda. If Kostak or STS appears without GMP, say GMP is unavailable.

## Core Math

Use upper price band unless a fixed price or final issue price is known.

```text
implied_listing_price = issue_price + gmp
gmp_pct = (gmp / issue_price) * 100
implied_gain_or_loss_per_share = gmp
implied_gain_or_loss_per_lot = gmp * lot_size
application_amount_per_lot = issue_price * lot_size
implied_listing_value_per_lot = implied_listing_price * lot_size
```

Examples:

| Issue Price | GMP | Lot Size | GMP % | Implied Listing Price | Per-Lot Gain/Loss |
|---:|---:|---:|---:|---:|---:|
| INR 500 | INR 50 | 30 | 10.0% | INR 550 | INR 1,500 gain |
| INR 240 | INR 0 | 62 | 0.0% | INR 240 | INR 0 |
| INR 300 | INR -15 | 50 | -5.0% | INR 285 | INR 750 loss |

## Disagreement Handling

If valid GMP sources differ, show:

- Lowest and highest GMP.
- Implied listing price range.
- GMP percentage range.
- Source spread as a percentage of issue price.

```text
source_spread = max(source_gmp) - min(source_gmp)
source_spread_pct_of_issue = (source_spread / issue_price) * 100
```

Do not average stale and fresh sources. If a row is stale, label it and either exclude it from the primary figure or show it separately.

## Interpretation Bands

These are sentiment labels, not return forecasts:

| GMP % | Interpretation |
|---:|---|
| More than 30% | Strong but speculative listing-sentiment signal |
| 10% to 30% | Moderate to strong signal, dependent on subscription quality |
| 5% to 10% | Weak positive signal |
| 0% to 5% | Noise-range GMP |
| 0% | Grey market is not pricing a premium |
| Negative | Grey market is pricing a discount |

Always attach the caveat that GMP can fail directionally or materially.
