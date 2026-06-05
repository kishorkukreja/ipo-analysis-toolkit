# Subscription Methodology

## Source Hierarchy

Use official, timestamped sources before secondary tables.

| Priority | Source | Use |
|---:|---|---|
| 1 | NSE/BSE issue pages and subscription files | Current and final category-wise subscription |
| 2 | NSE/BSE announcements and offer documents | Anchor allotment, price band, lot size, issue terms |
| 3 | Basis-of-allotment document and registrar updates | Final valid applications and allotment outcome |
| 4 | Chittorgarh, InvestorGain, IPOWatch, broker pages | Day-wise history and cross-checks when labeled secondary |
| 5 | Media and market commentary | Context only, never final numbers by itself |

If official exchange data and aggregator data disagree, prefer official exchange data with the latest timestamp and show a reconciliation note.

## Category Normalization

| Raw label | Normalized label |
|---|---|
| Qualified Institutional Buyers, QIB | QIB |
| Non Institutional Investors, NII, HNI | NII/HNI |
| Small NII, sNII, sHNI | sHNI/sNII |
| Big NII, bNII, bHNI | bHNI/bNII |
| Retail Individual Investors, RII, Retail | Retail/RII |
| EMP | Employee |
| Shareholder, Policyholder, Others | Reserved/Other |

Do not merge reserved categories into retail allotment odds unless the issue document explicitly defines them as part of retail.

## Day-Wise Reading

| Stage | Normal behavior | Interpretation |
|---|---|---|
| Day 1 | Retail may start early; QIB and NII may be quiet | Preliminary only; high Day 1 retail is not proof of quality |
| Day 2 | Retail becomes more meaningful; QIB may begin | QIB above 1x by Day 2 is constructive |
| Final day | QIB and NII can arrive late | Use timestamps; final-hour NII spikes may be leveraged |
| Post close | Final exchange numbers settle | Recheck against final exchange update and basis of allotment |

Never label intraday final-day data as final unless the source timestamp or final exchange document supports it.

## Mainboard Signal Matrix

| Pattern | Interpretation |
|---|---|
| High QIB, broad anchors, moderate/high retail | Higher-quality demand signal |
| High QIB, weak retail | Institutional interest but limited public enthusiasm |
| Weak QIB, high retail | Hype-led or GMP-led caution pattern |
| Weak QIB, high NII | Speculative or leverage-led caution pattern |
| High all categories | Hot issue, but retail allotment odds are likely poor |
| Low all categories | Weak demand unless valuation or fundamentals compensate |

Suggested mainboard thresholds:

| Category | Weak | Moderate | Strong | Extreme |
|---|---:|---:|---:|---:|
| QIB | <1x | 1-10x | 10-30x | >30x |
| Retail/RII | <1x | 1-5x | 5-15x | >15x |
| NII/HNI | <1x | 1-20x | 20-50x | >50x |

For NII/HNI above 50x, state that leverage and listing-gain trades may be involved. For NII/HNI above 100x, do not call the demand quality excellent without the leverage caveat.

## Data Freshness Labels

Use IST for IPO data.

| Label | Use |
|---|---|
| Live/intraday | Bidding window open and source can change |
| Near close | Final day data close to market close but not final |
| Final exchange update | Official post-close exchange data |
| Post basis-of-allotment | Basis-of-allotment or registrar data is available |

Required timestamp text:

```text
Data fetched: YYYY-MM-DD HH:MM IST
Source timestamp: YYYY-MM-DD HH:MM IST / Not shown by source
```
