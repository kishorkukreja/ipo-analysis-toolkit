---
name: ipo-gmp-tracker
description: Tracks and interprets Indian IPO grey market premium, implied listing price, GMP percentage, source agreement, trend, and reliability. Use when a user asks for IPO GMP, grey market premium, listing premium, expected listing price, GMP trend, Kostak, Subject-to-Sauda, or whether GMP supports an Indian IPO listing-sentiment view.
---

# IPO GMP Tracker

Use this skill for Indian IPO GMP analysis across NSE/BSE mainboard, NSE Emerge, and BSE SME issues. GMP is an informal sentiment signal only; never treat it as official, regulated, guaranteed, or sufficient for an apply/avoid recommendation.

## Required Inputs

Gather or infer:

- IPO name.
- IPO classification: mainboard, NSE SME, BSE SME, or unknown.
- Issue open date, close date, and listing date when relevant.
- Upper issue price or fixed issue price.
- Lot size.
- Current GMP from at least two reputable GMP sources when practical.
- Source timestamps or update labels.
- Subscription and QIB/NII/retail context when available.

If the IPO name, issue price, lot size, classification, or GMP source is missing and cannot be verified, state the missing field and ask for the exact IPO page or URL. Do not invent GMP.

## Source Workflow

1. Prefer live web verification for current GMP.
2. Check Tier 1 GMP sources first: Chittorgarh, InvestorGain, and IPOWatch.
3. If fewer than two usable Tier 1 sources are available, use Tier 2 trackers such as IPOMarket, IPO Rise, IPOsGMP.com, MainboardGMP, or Chanakya Ni Pothi.
4. Use NSE/BSE, registrar, offer documents, or reputable aggregators to verify IPO basics, listing timeline, and subscription context.
5. Do not use Groww or Zerodha MCP for GMP; they do not expose IPO-specific GMP data.
6. Exclude or label stale source rows. Do not silently average stale and fresh GMP figures.

Read when needed:

- `skills/shared/references/india_ipo_data_sources.md`
- `skills/shared/references/sme_vs_mainboard.md`
- `skills/ipo-gmp-tracker/references/gmp-methodology.md`
- `skills/ipo-gmp-tracker/references/source-and-reliability.md`
- `skills/ipo-gmp-tracker/references/trend-interpretation.md`
- `skills/ipo-gmp-tracker/assets/output-template.md`

## Calculations

Use the upper price band unless the issue is fixed-price or final issue price is known.

```text
implied_listing_price = issue_price + gmp
gmp_pct = (gmp / issue_price) * 100
implied_gain_or_loss_per_lot = gmp * lot_size
application_amount_per_lot = issue_price * lot_size
implied_listing_value_per_lot = implied_listing_price * lot_size
```

If sources disagree materially, show a GMP range and implied listing range instead of one false-precision number. If GMP is zero, say the grey market is not pricing a premium. If GMP is negative, compute the implied discount and loss per lot.

## Trend And Reliability

Build a day-wise trend when data exists: pre-open, Day 1, Day 2, final day, post-close, allotment day, final 24-48 hours, and listing morning. Classify as rising steadily, rising sharply, flat positive, flat zero, falling from high, volatile, divergent, or unknown.

Score reliability from 0 to 100 as confidence that GMP is a usable sentiment signal, not probability of profit. Apply hard caps:

- One source only: max Medium.
- SME plus one source only: max Low.
- Source spread above 8% of issue price: max Medium; max Low for SME.
- No timestamp and no trend: max Low.
- High GMP with weak QIB demand near close: max Low.
- Promotional, manipulation, or SEBI/order red flags: max Low.
- GMP-only answer without subscription or source context: max Medium.

## Timeline Rules

Use T+3 working days as the current default listing timeline, where T is issue close date. T+3 is mandatory for public issues opening on or after 2023-12-01. Mention T+6 only as historical context or if an older issue's offer document explicitly applies it.

For SME IPOs, identify the issue opening date. For issues opening on or after 2025-07-01, avoid older SME process assumptions and verify process-specific action points against exchange or SEBI sources when they affect the user.

## Output Rules

Return structured markdown using `assets/output-template.md`.

Always include:

- IPO snapshot with classification, price used, lot size, current GMP, GMP percent, implied listing price, implied per-lot gain/loss, listing timeline, and data freshness.
- Source cross-check table with URLs and timestamps.
- Trend interpretation.
- Reliability score and label.
- Separate facts, interpretation, and retail investor implications.
- Caveats that GMP is unofficial, unregulated, not guaranteed, and not enough for an apply/avoid decision.
- For SME IPOs: liquidity, lot-size, market-maker, spread, and manipulation caveats.

Never:

- Say GMP is official, regulated, guaranteed, safe, or confirmed.
- Give an apply/avoid verdict based only on GMP.
- Compute listing price from Kostak or Subject-to-Sauda.
- Hide missing data or stale timestamps.
- Present T+6 as the current default timeline.
