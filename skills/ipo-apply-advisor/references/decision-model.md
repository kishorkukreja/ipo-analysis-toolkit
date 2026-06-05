# Decision Model

## Core Framing

Produce two conclusions before the final verdict:

- Listing-gain view: short-term demand, GMP support, subscription quality, anchor quality, market context, issue size/float, and liquidity.
- Long-term subscribe view: business quality, financial quality, governance, valuation, cash conversion, use of proceeds, and risk durability.

Final decision mapping:

| Listing view | Long-term view | Final decision |
|---|---|---|
| Strong | Strong | Apply |
| Strong | Moderate | Apply for listing gains, with long-term caution |
| Strong | Weak | Neutral, or Avoid if any auto-avoid gate fires |
| Moderate | Strong | Neutral or Apply only if user accepts holding risk |
| Weak | Strong | Neutral or wait for listing |
| Weak | Weak | Avoid |

`Apply for listing gains` is not the same as `Subscribe for long term`.

## Auto-Avoid Gates

Any one of these normally forces `Avoid`, regardless of GMP or subscription:

- Active SEBI/ED/serious criminal action against promoter or issuer.
- Negative operating cash flow in 2 of last 3 years while reporting profits.
- OCF/PAT materially below 0.4 for multiple years without clear working-capital explanation.
- Promoter pledge above 75% of promoter holding.
- Material auditor qualification affecting going concern, revenue, inventory, receivables, or related parties.
- Financial restatement above 10% of revenue or profit.
- RPTs above 30% of revenue without strong arm's-length evidence.
- SME IPO with sudden profit spike, weak auditor, large RPTs, and no credible institutional filter.
- Pure or near-pure OFS with weak growth need and expensive valuation.
- IPO proceeds routed to promoter/related-party debt or entities.
- Regulatory model risk that can impair core revenue immediately.

If a user explicitly asks for a speculative listing-gain-only view, keep the core verdict `Avoid` when a hard gate fires and label the trade as speculation.

## Weighted Score

Use this after gates:

| Component | Weight | Strong signal |
|---|---:|---|
| Financial quality | 25 | durable growth, margins, returns, cash conversion, sector-appropriate leverage |
| Valuation | 20 | fair/discounted vs direct peers, justified premium, correct multiple |
| Governance and issue structure | 20 | clean auditors, low RPTs/pledge/litigation, growth-oriented fresh issue |
| Demand quality | 15 | strong QIB, credible anchors, balanced subscription, not just retail hype |
| GMP/listing sentiment | 10 | stable/rising, corroborated, never official |
| Market/liquidity adjustment | 10 | supportive market, adequate float, mainboard depth, manageable SME liquidity |

Score interpretation:

| Score | Base interpretation |
|---:|---|
| 80-100 | Apply if no severe unresolved caveat |
| 65-79 | Apply or Neutral depending on contradictions and confidence |
| 50-64 | Neutral, horizon-specific only |
| 35-49 | Avoid unless short-term demand is exceptional and risks are accepted |
| 0-34 | Avoid |

For SME IPOs, subtract 5-15 points for liquidity, lot-size, and disclosure risk. Cap confidence at Medium unless audited history, cash conversion, merchant banker quality, and institutional/anchor demand are strong. If valuation is above peer median and GMP is the main positive, cap final decision at Neutral.

## Listing-Gain Labels

Use GMP level/trend, QIB/NII/retail subscription, anchor quality, market mood, issue size/float, SME/mainboard liquidity, and valuation overhang.

| Score | Label |
|---:|---|
| 75+ | Strong listing-gain setup |
| 60-74 | Moderate listing-gain setup |
| 45-59 | Unclear listing setup |
| <45 | Weak listing setup |

## Long-Term Labels

Use business quality, financial score, cash conversion, valuation, governance, use of proceeds, moat, and lock-in overhang.

| Score | Label |
|---:|---|
| 75+ | Long-term subscribe candidate |
| 60-74 | Holdable but needs valuation/risk caveat |
| 45-59 | Speculative or wait for listing |
| <45 | Not investable |

## Contradiction Handling

- High GMP, weak fundamentals: Neutral or Avoid. For SME, usually Avoid or Neutral, not Apply.
- Strong fundamentals, no GMP: Neutral for listing gains; possible long-term apply only if valuation is attractive.
- Strong QIB, weak retail: favor long-term if fair value; do not promise a large listing pop.
- High retail/NII, weak QIB: downgrade demand quality as hype or leveraged demand.
- Good financials, expensive valuation: Neutral unless premium is justified by margin, returns, and cash flow.
- Cheap valuation, poor governance: value trap; Avoid if governance issue is material.
- Strong anchors, lock-in overhang: improve listing score but add 30-day/90-day supply caveat if disclosed.

## Confidence

High confidence requires primary documents, current exchange subscription data, direct peer set, multi-day GMP corroboration, and no major contradictions.

Cap confidence at Medium or Low when:

- IPO is SME and disclosures/demand quality are thin.
- GMP is the main positive signal.
- Subscription is early or timestamp missing.
- Peer set is weak or old.
- Primary offer document is missing.
- Major contradictions remain unresolved.
