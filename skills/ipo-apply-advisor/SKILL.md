---
name: ipo-apply-advisor
description: Use when advising whether to apply, avoid, or stay neutral on an Indian IPO using prior IPO skill outputs or fresh sources. Covers NSE/BSE mainboard and SME IPOs, listing-gain vs long-term framing, GMP/subscription caveats, category/cut-off guidance, and the mandatory final verdict block.
---

# IPO Apply Advisor

Use this skill for Indian IPO decision synthesis. It is the final advisor layer after, or instead of, financial scoring, red-flag detection, peer valuation, GMP tracking, and subscription tracking.

## First Move

Open with a bias check unless the user already gave a neutral analysis request:

```text
Before I answer: are you leaning Apply, Avoid, or undecided? I will pressure-test that bias against the evidence.
```

If the user wants an immediate answer, proceed and set `Bias adjusted` according to whether a bias was tested. Do not delay urgent or one-shot requests just to ask a question.

## Inputs To Reuse

Reuse prior outputs in the conversation when present:

- `ipo-financials-scorer`
- `ipo-red-flags-detector`
- `ipo-peer-comparison`
- `ipo-gmp-tracker`
- `ipo-subscription-tracker`

When a dependent output is missing, fill the gap inline from primary sources if possible. If current data or IPO-specific details are needed, browse or fetch current sources. If the user supplies a DRHP/RHP/prospectus URL, use it before searching. If a required offer document cannot be found, ask for the exact URL instead of inventing facts.

Load references only as needed:

- `references/decision-model.md` for scoring, auto-avoid gates, and contradiction handling.
- `skills/shared/references/ipo_scorecard_model.md` for 0-100 department scores, weights, confidence caps, and hard gates.
- `references/category-and-process.md` for retail/sHNI/bHNI, SME, cut-off, T+3, ASBA/UPI, and July 2025 SME process rules.
- `references/source-and-safety.md` for source hierarchy, caveats, and advice boundaries.
- `assets/output-template.md` for the required response shape.

Also use shared references when useful:

- `skills/shared/references/india_ipo_data_sources.md`
- `skills/shared/references/sme_vs_mainboard.md`
- `skills/shared/references/registrars.md`

## Workflow

1. Classify the issue as mainboard, NSE Emerge, BSE SME, or unknown. If unknown, treat classification as a required lookup.
2. State data freshness: date checked, issue stage, and source timestamps for subscription/GMP when available.
3. Build separate views:
   - Listing-gain view: GMP level/trend, QIB/NII/retail demand quality, anchors, market mood, issue size/float, valuation overhang, and SME liquidity.
   - Long-term subscribe view: business quality, financials, cash conversion, valuation, governance, use of proceeds, moat, and post-listing supply overhang.
4. Run auto-avoid gates before weighted scoring. Severe governance, cash-conversion, auditor, RPT, pledge, restatement, regulatory, or SME manipulation patterns can force `Avoid` regardless of GMP.
5. Score only after gates using 0-100 department scores and the shared weighted model: financial quality 25%, valuation 20%, governance/issue structure 20%, demand quality 15%, GMP/listing sentiment 10%, and application/liquidity/timeline risk 10%.
6. Resolve contradictions conservatively. High GMP cannot offset weak fundamentals or hard red flags. Strong fundamentals with weak demand often means `Neutral` or wait for listing.
7. Give practical category and capital guidance: Retail, sHNI, bHNI, SME individual, or not recommended. Calculate amount as `lot size x bid price x lots`; for cut-off retail examples use the upper band unless a different bid price is stated.
8. Give cut-off price guidance. For book-built mainboard retail applications, default to cut-off only if the apply thesis survives upper-band valuation.
9. End with the mandatory `## Verdict` table exactly as described in `assets/output-template.md`.

## Decision Rules

- `Apply`: no auto-avoid trigger, acceptable valuation, clean or manageable governance, and either strong long-term case or strong listing setup with risk clearly bounded.
- `Neutral`: weighted score 55-74, mixed evidence, missing primary data, conflicting market signals, early subscription data, strong listing but weak long-term quality, strong fundamentals but weak demand, or unresolved contradictions.
- `Avoid`: auto-avoid trigger, poor cash conversion, material governance concern, expensive weak business, retail/NII hype with weak QIB, or SME risk stack dominated by GMP.

Do not issue `Apply` from a raw weighted score when a hard gate fires or when confidence is Low because primary documents, official subscription data, or market-signal timestamps are missing.

For SME IPOs, lower confidence by default, include liquidity/exit risk, verify issue open date, and apply July 2025 revised process guidance for issues opening on or after 2025-07-01.

## Safety Boundary

Provide research support, not personal financial advice. Do not guarantee allotment, listing gains, GMP reliability, or returns. Do not tell the user to deploy more capital solely to improve allotment odds. Flag payment-route and category feasibility instead.
