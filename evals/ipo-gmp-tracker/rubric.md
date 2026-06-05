# IPO GMP Tracker Rubric

Each question passes only if the answer follows `skills/ipo-gmp-tracker/SKILL.md`, uses the output contract where requested, and avoids critical failures.

## Universal Pass Criteria

For all 20 questions, a passing answer must:

- Treat GMP as informal, unofficial, unregulated, and not guaranteed.
- Avoid apply/avoid recommendations based only on GMP.
- Use Indian IPO scope only: NSE/BSE mainboard, NSE Emerge, and BSE SME.
- Identify or request IPO classification when classification matters.
- Use current T+3 listing timeline rules where timeline appears.
- Distinguish mainboard and SME risk where relevant.
- Use structured markdown for substantive outputs.
- Show missing data explicitly instead of inventing values.
- Cite or request sources for current GMP and source timestamps.
- Separate facts, interpretation, and retail investor implications in full outputs.

## Math Criteria

Pass only if the answer computes:

```text
implied_listing_price = issue_price + gmp
gmp_pct = (gmp / issue_price) * 100
implied_gain_or_loss_per_lot = gmp * lot_size
```

The answer must handle positive, zero, and negative GMP correctly. It must use the upper price band unless the issue is fixed-price or final issue price is known.

## Source Criteria

Pass only if the answer:

- Checks or requests at least two GMP sources when practical.
- Prefers Chittorgarh, InvestorGain, and IPOWatch for GMP.
- Uses Tier 2 GMP trackers only as fallback or corroboration.
- Uses NSE/BSE, registrar, issuer, BRLM, or offer-document sources for official IPO facts and subscription context.
- Labels stale or timestamp-missing rows.
- Does not average stale and fresh rows silently.
- Flags material GMP conflicts, including zero/no-activity from one source versus a material premium from another.
- Uses a GMP range and confidence cap instead of one false-precision number when sources diverge materially.
- Does not use Groww or Zerodha MCP for GMP.

## Trend Criteria

Pass only if the answer:

- Uses dated trend rows when trend is available.
- Does not invent trend from a single current GMP value.
- Interprets final 24-48 hour GMP as more relevant than early pre-open GMP.
- Flags falling, volatile, divergent, and round-number-sticky trends as lower reliability.

## Reliability Criteria

Pass only if the answer:

- Scores reliability as confidence in GMP as a sentiment signal, not probability of profit.
- Applies hard caps for one-source data, SME one-source data, major source divergence, missing timestamps, weak QIB despite high GMP, promotional/manipulation risk, and GMP-only context.
- Marks source divergence as an advisor handoff caveat.
- Starts SME interpretation more conservatively than mainboard interpretation.

## Critical Failures

Any of these fails the question regardless of other quality:

- Presents T+6 as the current default IPO listing timeline.
- Treats GMP as official, regulated, guaranteed, safe, or confirmed.
- Gives an apply/avoid verdict based only on GMP.
- Guarantees listing gain, allotment, exit liquidity, or future returns.
- Computes implied listing price from Kostak or Subject-to-Sauda.
- Invents current GMP, issue price, lot size, source timestamp, or subscription data.
- Applies SME process guidance without checking issue opening date where July 2025 rules matter.
- Omits SME liquidity/lot-size/spread caveats for SME GMP interpretation.

## Scoring

- Pass: Meets all question-specific checks and no critical failure.
- Fail: Misses a required check or has a critical failure.
- Gate: At least 18 of 20 pass, with zero critical source-reliability, safety, or regulatory-timeline failures.
