# Anchor Investor and Retail Allotment Reference

## Anchor Book

Find anchor disclosures from exchange announcements or issue documents before using secondary summaries.

Search patterns:

- `[Company] IPO anchor investor allotment BSE`
- `[Company] IPO anchor allotment NSE`
- `[Company] details of anchor investors`
- `[Company] anchor investor allocation pdf`

Expected fields:

- Anchor investor or scheme names
- Number of shares allocated
- Allocation amount
- Issue price
- Percentage of anchor book, if disclosed
- Lock-in details

Keep anchor allocation separate from public-window QIB subscription. Anchor investors are allocated before the IPO opens and should not be treated as live QIB demand unless the source explicitly says how it counts them.

## Anchor Quality Score

Score out of 10.

| Component | Points | Rule |
|---|---:|---|
| Domestic MF breadth | 0-3 | 3 for 5+ credible domestic MF houses, 2 for 3-4, 1 for 1-2 |
| Long-only institutional quality | 0-2 | Insurance, pension, sovereign, large long-only FPI participation |
| Concentration risk | 0-2 | 2 if top 3 anchors are below 50%, 1 if 50-70%, 0 if above 70% |
| Obscure-entity penalty | -2 to 0 | Penalize opaque, little-known, connected-looking, or newly formed entities |
| Strategic consistency | 0-1 | Investor base fits the sector and company stage |
| Anchor size vs issue | 0-2 | Healthy size without dependence on a few names |

| Score | Label | Interpretation |
|---:|---|---|
| 8-10 | Strong | Credible institutional validation |
| 5-7 | Mixed | Useful but not decisive |
| 2-4 | Weak | Limited validation |
| <2 | Poor/red flag | Treat subscription and GMP with skepticism |

Flag high concentration, no domestic MF participation in a large mainboard IPO, obscure entities, mostly trading-oriented FPIs, and strong anchor demand followed by weak final QIB subscription.

Anchor lock-in note for current Indian IPOs:

- 50% of anchor allocation: locked for 30 days from allotment.
- Remaining 50%: locked for 90 days from allotment.

## Retail Allotment Estimate

Preferred formula:

```text
available_lots = floor(retail_shares_available / minimum_lot_size)
probability = min(100%, available_lots / valid_retail_applications * 100)
```

Fallback proxy when valid application count is unavailable:

```text
probability_proxy = min(100%, 100 / retail_subscription_multiple)
```

Label the method used. The proxy assumes an average retail application near one lot and can be wrong when many applicants bid multiple lots.

| Retail subscription | Probability language |
|---:|---|
| <1.0x | High; full allotment likely if valid |
| 1.0-2.0x | Good, but scaling or lottery may apply |
| 2.0-5.0x | Moderate lottery |
| 5.0-10.0x | Low lottery |
| 10.0-30.0x | Very low lottery |
| >30.0x | Long-shot lottery |

Allowed family-account guidance: separate genuine applications from separate PAN/demat/bank accounts can increase household entries. Do not suggest duplicate applications under the same PAN or any workaround.

## NII/HNI Allotment Caveat

Do not present HNI allotment as simply proportional. Current NII allotment mechanics include minimum-application lots and proportionate allocation of remaining shares where applicable. Split sHNI/sNII and bHNI/bNII when source data exposes the split.

For leveraged HNI applications, explain:

```text
net_hni_gain = listing_gain - funding_cost - brokerage/taxes/charges
```

High NII subscription may support sentiment, but it is not a clean quality signal.
