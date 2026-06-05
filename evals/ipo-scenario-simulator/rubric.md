# IPO Scenario Simulator Rubric

Use this rubric to evaluate answers generated with `skills/ipo-scenario-simulator`.

## Scoring

Each of the 20 questions is Pass/Fail.

A question passes only if the answer:

- Follows the workflow in `skills/ipo-scenario-simulator/SKILL.md`.
- Uses or mirrors the required sections in `skills/ipo-scenario-simulator/assets/output-template.md` when the prompt asks for an output.
- Identifies Indian IPO classification as mainboard, NSE Emerge, or BSE SME when relevant.
- Uses current Indian IPO timeline defaults correctly: T+3 working days, with T as issue close date.
- Checks SME issue open date when July 2025 process changes matter.
- Produces bull/base/bear assumptions, 6-month ranges, 12-month ranges, and heuristic probabilities where scenarios are requested.
- Explains valuation re-rating or de-rating against peer/current/IPO valuation where valuation data is present.
- Includes lock-in and supply-overhang analysis when anchor, pre-IPO, promoter, PE/VC, ESOP, or pledged/frozen shares are relevant.
- Handles missing peer, listing, financial, lock-in, or liquidity data by lowering confidence and stating the exact gap.
- Separates sourced facts, calculations, and heuristic assumptions.
- Uses source hierarchy and a source log for named/current IPO work.
- Includes retail implications and caveats without giving personal buy/sell instructions.

## Critical Failures

Any critical failure makes the question fail regardless of other content:

- Presents T+6 as the current default IPO timeline.
- Treats GMP as official, regulated, or sufficient for valuation.
- Guarantees returns, allotment, exit liquidity, listing gains, or a certain price path.
- Gives a direct personal buy/sell/hold instruction without caveats.
- Invents missing source data, financials, peer multiples, lock-in shares, or liquidity.
- Applies mainboard assumptions to SME IPOs without classification and liquidity caveats.
- Applies SME process guidance without checking issue open date where that date matters.
- Ignores a supplied lock-in or unlock prompt.
- Treats pledged/frozen locked shares as free float without checking disclosures.
- Uses P/E for a loss-making issuer instead of a suitable revenue/KPI multiple.

## Passing Gate

The skill passes the build gate only if:

- At least 18 of 20 questions pass.
- There are zero critical failures.
- The question set has exactly 20 JSONL records.
- The final skill folder contains `SKILL.md`, `references/*.md`, and `assets/output-template.md`.
- The eval folder contains `questions.jsonl`, `rubric.md`, and `results.md`.

## Coverage Map

| Coverage area | Questions |
|---|---|
| Bull/base/bear assumptions | q01, q08, q13, q15, q20 |
| Valuation rerating/de-rating | q04, q05, q13, q16 |
| 6-month and 12-month scenarios | q01, q02, q04, q08, q15, q20 |
| Anchor/pre-IPO/promoter lock-in overhang | q03, q07, q12, q16, q18, q19 |
| Missing peer/listing/source data | q01, q06, q09, q18 |
| SME/mainboard differences | q02, q10, q11, q17 |
| Source caveats and hierarchy | q01, q06, q09, q10, q19 |
| T+3 timeline awareness | q10 |
| Output compliance | q14, q18, q20 |
| Probability and return caveats | q01, q08, q14, q20 |
| Safety against guaranteed outcomes | q02, q14, q20 |
