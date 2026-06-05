# Source And Reliability Framework

## Source Hierarchy

### Tier 1 GMP Sources

| Source | URL | Best Use | Caveat |
|---|---|---|---|
| Chittorgarh | https://www.chittorgarh.com/ipo/ipo_gmp.asp | Baseline GMP and archives | Informal grey-market data, may lag |
| InvestorGain | https://www.investorgain.com/report/ipo-gmp-live/331/ipo/undefined/ | Current GMP, timestamps, SME/mainboard rows | Informational only |
| IPOWatch | https://ipowatch.in/ipo-grey-market-premium-chittorgarh-com/ | Cross-check and archive context | Verify page freshness |

### Tier 2 GMP Sources

Use when Tier 1 has fewer than two usable rows:

- IPOMarket: https://www.ipomarket.in/gmp
- IPO Rise: https://www.iporise.com/gmp
- IPOsGMP.com: https://iposgmp.com/
- MainboardGMP: https://mainboardgmp.com/
- Chanakya Ni Pothi: https://chanakyanipothi.com/property-share-invit-ipo-gmp/

### Official And Subscription Cross-Checks

Official sources usually do not publish GMP, but they help test whether GMP is plausible:

- NSE IPO pages: https://www.nseindia.com/market-data/new-issues-ipo
- NSE upcoming issues: https://www.nseindia.com/market-data/all-upcoming-issues-ipo
- BSE public issues: https://www.bseindia.com/publicissue.html
- BSE IPO process/status: https://www.bseindia.com/markets/PublicIssues/IPOProcess_Status.aspx
- Registrar, issuer, BRLM, and offer-document pages.

## Freshness Labels

| IPO Stage | Target Freshness | Label |
|---|---:|---|
| Not yet open | 24 hours | Early/exploratory GMP |
| Day 1 | 6-12 hours | Noisy GMP |
| Day 2 | 4-8 hours | Developing GMP |
| Final subscription day | 1-4 hours | Active GMP |
| Post-close to allotment | 6-12 hours | Stabilizing GMP |
| Final 24-48 hours before listing | 1-6 hours | Most relevant GMP |
| Listing morning | Under 2 hours where available | Last-look GMP |

If all timestamps are missing, set freshness to unknown and cap reliability at Low unless the user explicitly asked only for a quick non-decision figure.

## Reliability Score

Start at 50. Adjust:

| Driver | Adjustment |
|---|---:|
| 3+ credible sources agree within 3% of issue price | +15 |
| 2 credible sources agree within 3% of issue price | +8 |
| Only 1 source available | -15 |
| Sources diverge by more than 8% of issue price | -20 |
| Latest timestamp within target window | +10 |
| Stale for stage | -10 |
| Timestamp missing on all sources | -15 |
| Stable or rising trend over final 24-48 hours | +10 |
| Steady but early trend | +5 |
| Volatile trend | -10 |
| Falling sharply into listing | -15 |
| QIB/subscription quality supports GMP | +15 |
| Total and retail demand support GMP | +8 |
| High GMP but weak subscription | -10 |
| High GMP and QIB below 1x near close | -15 |
| SME IPO | -10 |
| Very small mainboard issue | -5 |
| SME plus small issue plus one-source GMP | -15 |
| Broader market stable or positive near listing | +5 |
| Broader market sharply weak near listing | -10 |
| Promotional noise, round-number stickiness, or suspicious Kostak/STS mismatch | -10 |
| Clear pump/manipulation allegation, SEBI order, or similar red flag | -20 |

Map scores:

| Score | Label |
|---:|---|
| 75-100 | High |
| 55-74 | Medium |
| 35-54 | Low |
| 0-34 | Very Low |

The score means confidence that GMP is a usable sentiment signal. It is not the probability of listing gain.

## Hard Caps

- One source only: max Medium.
- SME IPO with one source only: max Low.
- Source divergence above 8% of issue price: max Medium, or Low for SME.
- No timestamp and no trend: max Low.
- GMP high while QIB is below 1x near final day: max Low.
- Promotional/manipulation red flags: max Low.
- Grey-market-only answer without source and subscription context: max Medium.
