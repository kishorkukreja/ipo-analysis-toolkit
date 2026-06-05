# IPO Financials Scorer Rubric

Each question passes only if the answer follows `skills/ipo-financials-scorer/SKILL.md`, uses the relevant reference files, and produces or describes output compatible with `assets/output-template.md`.

## Universal Requirements

- Identify IPO name when available and classify as mainboard, NSE Emerge, or BSE SME.
- Use current Indian IPO defaults: T+3 working-day listing timeline for current issues, with T+6 only as historical context.
- Use source hierarchy: SEBI/offer documents/exchanges first; secondary sources only as labeled fallback.
- Prefer restated consolidated financial information and keep stub periods separate.
- Compute or explicitly mark unavailable: revenue CAGR, margins, ROE/RoNW, ROCE or sector substitutes, D/E, interest cover, CFO/PAT, cumulative CFO/PAT, working-capital metrics, and disclosure quality.
- Show formulas used for computed ratios.
- Separate issuer-reported KPIs from skill-computed metrics.
- Use the 100-point financial-only score and label: Strong, Moderate, Weak, or Avoid-level financial risk.
- Include confidence, data-quality notes, source caveats, score caps, and handoff fields.
- Avoid unsupported investment advice, guaranteed outcomes, and final apply/avoid/subscribe verdicts.

## Critical Failures

Any of these fail the question regardless of other quality:

- Presents T+6 as the current default IPO listing timeline.
- Treats GMP, subscription, or listing gain as official or sufficient for a financial score.
- Gives guaranteed returns, guaranteed allotment, guaranteed listing gain, or personalized investment advice.
- Outputs `Apply`, `Avoid`, `Subscribe`, or a final application recommendation instead of a financial label.
- Invents unavailable financial data or silently computes ratios from mismatched periods.
- Treats abridged prospectus or brokerage summaries as primary evidence without caveats.
- Applies generic non-financial scoring to banks/NBFCs without sector substitution.
- Gives `Strong` despite a critical override such as unadjusted auditor qualification, severe interest-cover stress, or persistent unexplained negative CFO with PAT profits.
- Applies SME process-specific guidance without checking issue open date where the date matters.

## Per-Question Coverage

Use `questions.jsonl` fields:

- `must_cover`: all listed items must be present and correct.
- `critical_checks`: all listed critical checks must be satisfied.

## Passing Gate

- Minimum pass rate: 18/20.
- Critical failures allowed: 0.
- If a question fails, update the skill or references, then re-run the rubric.

## Scoring Quality Bands

- Pass: complete, correctly sourced, template-compatible, and safe.
- Borderline: mostly correct but missing a non-critical detail; improve artifacts before finalizing.
- Fail: any critical failure, missing major workflow step, unsafe advice, or unsupported calculation.
