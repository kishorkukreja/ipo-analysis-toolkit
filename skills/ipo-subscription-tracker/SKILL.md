---
name: ipo-subscription-tracker
description: Track and interpret Indian IPO subscription data, day-wise demand, anchor investor quality, retail allotment odds, and cutoff bidding implications for NSE/BSE mainboard and SME IPOs.
---

# IPO Subscription Tracker

Use this skill when the user asks about Indian IPO subscription status, category-wise demand, day-wise subscription trends, anchor investors, retail allotment probability, HNI/NII demand, or whether to bid at cutoff price.

## Read First

- `skills/shared/references/india_ipo_data_sources.md`
- `skills/shared/references/sme_vs_mainboard.md`
- `skills/ipo-subscription-tracker/references/subscription-methodology.md`
- `skills/ipo-subscription-tracker/references/anchor-and-allotment.md`
- `skills/ipo-subscription-tracker/references/sme-and-bidding-rules.md`
- `skills/ipo-subscription-tracker/assets/output-template.md`

## Workflow

1. Identify the IPO, symbol if known, issue type, listing platform, issue open date, issue close date, price band, lot size, and minimum application amount.
2. Classify the issue as mainboard, NSE SME/Emerge, or BSE SME before interpreting the data. If classification is unknown and cannot be verified, say it is a required lookup.
3. For live or current IPO data, browse or fetch current sources. Prefer official NSE/BSE issue pages, exchange filings, anchor allotment announcements, and basis-of-allotment documents. Use Chittorgarh, InvestorGain, IPOWatch, broker pages, or media only as labeled secondary sources.
4. Capture freshness in IST: data fetched time, source timestamp when available, and status such as live/intraday, near close, final exchange update, or post basis-of-allotment.
5. Normalize category labels into QIB, NII/HNI, sHNI/sNII, bHNI/bNII, Retail/RII, Employee, Shareholder/Policyholder/Other, and Total.
6. Keep the anchor book separate from public-window QIB subscription unless a source explicitly explains that it includes anchor allocation.
7. Reconcile official sources before aggregators. If NSE, BSE, and aggregator numbers conflict, show the discrepancy, prefer the latest official timestamp, and do not call the data final unless final exchange or allotment documents support it.
8. Estimate retail allotment odds using valid retail applications and available retail minimum lots when available. If not available, use `min(100%, 100 / retail_subscription_multiple)` as a proxy and label it clearly.
9. Interpret subscription as a demand signal, not a complete investment decision. Do not issue an Apply/Avoid verdict unless the user explicitly asks; even then, state that final advice belongs in `ipo-apply-advisor`.
10. For current IPO timelines, use T+3 working days from issue close. T+3 is mandatory for public issues opening on or after 2023-12-01. Mention T+6 only as historical or issue-specific legacy context.

## Interpretation Rules

- QIB demand is the cleanest subscription quality signal, especially final-day QIB demand.
- Retail subscription mainly informs public enthusiasm and allotment odds; it is weak as a standalone quality signal.
- NII/HNI demand can be leverage-driven. Treat NII above 50x as likely hot money and NII above 100x as a poor standalone quality signal.
- Strong anchor participation is useful only when quality is broad and credible. Score investor type, concentration, domestic MF breadth, and obscure-entity risk.
- High subscription plus weak QIB is a caution pattern, especially when GMP or retail enthusiasm is driving the narrative.
- GMP is informal and unregulated. Keep it separate from official subscription data.

## SME Handling

For every SME IPO, add a stricter risk layer:

- State whether it is NSE SME/Emerge or BSE SME.
- Show lot value and minimum application amount.
- Add liquidity, spread, small-float, and market-maker caveats.
- Do not apply mainboard subscription thresholds mechanically.
- For issues opening on or after 2025-07-01, verify current SME bidding mechanics from exchange/SEBI or issue documents before advising on cutoff bidding, bid revision, cancellation, or final-day timing.
- If the July 2025 process detail is not verified for the issue, say what is unknown and avoid specific application instructions.

## Cutoff vs Price Bidding

- For mainboard book-built retail applications where cutoff bidding is available, explain that cutoff means accepting the final issue price within the price band. It helps avoid rejection from bidding below the discovered price; it does not improve lottery odds after a valid application is in the retail pool.
- If the user bids a specific price below the final issue price, the bid may be invalid or not considered. If they bid at the cap, cash blocking may be similar to cutoff.
- Do not recommend cutoff bidding for fixed-price issues or SME issues unless the issue documents or official platform rules confirm it is available.
- Explain category limits: retail is up to Rs 2 lakh; sHNI/sNII and bHNI/bNII have different amount bands and allotment mechanics.

## Missing Data Behavior

- If no live data can be verified, provide the exact source needed: exchange issue page, exchange announcement, RHP/prospectus, registrar page, or aggregator link.
- Do not invent subscription multiples, anchor names, issue dates, lot size, or allotment probability.
- If only secondary data is available, label confidence as Medium or Low and name the missing official source.
- If timestamps are missing, state the fetch time and say the source did not expose its own timestamp.

## Required Output

Follow `skills/ipo-subscription-tracker/assets/output-template.md`. Always include:

- Snapshot
- Source Checks
- Subscription
- Day-Wise Trend
- Anchor Book
- Retail Allotment Estimate
- Cutoff vs Price Bidding
- Interpretation
- Source Reconciliation
- Investor Takeaway
- Caveats and Missing Data

End with demand quality, allotment odds, data confidence, and caveats. Avoid guaranteed allotment, guaranteed listing gains, or personalized financial advice.
