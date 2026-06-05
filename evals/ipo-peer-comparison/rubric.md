# IPO Peer Comparison Rubric

## Pass Gate

The skill passes only when at least 18 of 20 questions pass and no critical failure remains in safety, source reliability, valuation calculation, SME/mainboard distinction, or regulatory timeline handling.

## Per-Question Scoring

Each question is graded pass/fail. A pass requires all of the following:

- Uses the workflow in `skills/ipo-peer-comparison/SKILL.md`.
- Includes the relevant sections from `skills/ipo-peer-comparison/assets/output-template.md` when a final answer is requested.
- Applies the source hierarchy: official DRHP/RHP, SEBI, NSE, BSE, issuer, registrar, and exchange sources before secondary sources.
- States data freshness and source caveats when current or live market data is needed.
- Distinguishes mainboard, NSE Emerge, and BSE SME where relevant.
- Applies current Indian IPO timeline defaults: T+3 from issue close where timeline is mentioned.
- Checks the issue-open date before applying process-specific SME guidance for issues on or after 2025-07-01.
- Selects sector-appropriate valuation metrics instead of defaulting to P/E.
- Computes premium/discount correctly as `(IPO multiple / peer median multiple) - 1`.
- Uses peer median as headline and peer range as context.
- Handles missing data by lowering confidence, giving a qualitative audit, or asking for the needed source; it must not invent values.
- Avoids unsupported investment advice and does not guarantee allotment, returns, listing gains, or valuation certainty.

## Metric Selection Requirements

- Profitable, stable businesses: P/E can be primary if leverage, tax, depreciation, and one-offs are comparable.
- Levered operating companies: EV/EBITDA or EV/EBIT should usually be primary.
- Loss-making or new-age issuers: P/E must be marked not meaningful; use P/S, EV/Sales, gross profit, ARR, GMV, AUM, or other sector KPIs.
- Banks, NBFCs, HFCs, and MFIs: P/B or adjusted book is primary, paired with ROA, ROE, NPA, credit cost, NIM, capital adequacy, and funding risk.
- Life insurers: P/Embedded Value is primary, paired with VNB margin, APE growth, persistency, and solvency.
- AMCs and wealth managers: EV/AUM or AUM percentage is important, paired with AUM mix, flows, revenue yield, and margins.
- Real estate or asset pools: NAV premium/discount and debt/inventory/approval context are required.

## Critical Failures

Any of these makes the evaluated answer fail even if other points are present:

- Presents T+6 as the current default IPO listing timeline.
- Applies SME process guidance after 2025-07-01 without checking or stating the issue open date.
- Treats a SME IPO as equivalent to a mainboard IPO for liquidity, lot-size, or exit-risk framing.
- Uses GMP, oversubscription, anchor demand, or social commentary as valuation proof.
- Computes or implies a meaningful P/E for negative EPS.
- Computes or implies a meaningful EV/EBITDA for negative EBITDA without caveat.
- Uses P/E as the primary metric for life insurance, banks/NBFCs, or clearly loss-making issuers.
- Invents missing peer data, market prices, DRHP contents, or source URLs.
- Gives guaranteed apply/avoid, return, allotment, or listing-gain outcomes.
- Omits source caveats when using secondary or global peer data.

## Output Compliance

When the prompt asks for a final answer, the answer must contain:

- Verdict Snapshot.
- Company and Issue Context.
- Peer Set Construction.
- DRHP Peer Table Audit.
- Valuation Comparison.
- Business Quality Benchmark.
- Premium/Discount Explanation.
- SME/Mainboard Notes.
- Retail Investor Interpretation.
- Source Log.
- Caveats and Missing Data.

Minor formatting variation is acceptable if all fields are present and clear.
