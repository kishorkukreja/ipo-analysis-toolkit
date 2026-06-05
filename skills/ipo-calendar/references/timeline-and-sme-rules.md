# Timeline and SME Rules

## Current IPO Timeline

Use T+3 working days as the current default public issue listing timeline. T is the issue closing date.

Official anchor:

- SEBI circular SEBI/HO/CFD/TPD1/CIR/P/2023/140 dated 2023-08-09 reduced the listing timeline for public issues from T+6 to T+3 working days.
- T+3 is the default for current IPO calendar work. Treat T+6 as historical unless analyzing an older issue or a source explicitly tied to an older timeline.

## Calendar Use

When dates are available from official issue documents, exchange notices, or registrar notices, use the official dates.

When dates must be computed:

- Mark every computed date as "expected".
- Use working days, not calendar days.
- Warn that market holidays, issue extension, price-band revision, registrar processing, or exchange approval can change dates.
- Do not guarantee allotment, refund, demat credit, or listing.

Typical T+3 sequence:

| Event | Timing |
|---|---|
| Issue closes | T |
| Basis of allotment | Expected around T+1 |
| Refund / UPI unblock | Expected around T+2 |
| Demat credit | Expected around T+2 |
| Listing | Expected around T+3 |

## IPO Stage Labels

Use these labels consistently across calendar, subscription, application, allotment, listing-day, and apply-advisor outputs:

| Stage | Meaning | Main caveat |
|---|---|---|
| Pre-open | Issue terms known, bidding not open | No subscription signal yet |
| Day 1 / opening day | First bidding day | Retail/NII can move early; QIB often builds later |
| Middle days | Open but not final day | Trend is forming, not final |
| Final day | Last bidding day | Distinguish intraday from final exchange data |
| Post-close / pre-allotment | Bidding closed, basis pending | Use final data when available; allotment still unconfirmed |
| Post-allotment / pre-listing | Allotment done, listing pending | Focus on demat/refund/listing setup |
| Listed | Trading started | IPO application/allotment guidance is historical |

## SME Classification

Always classify SME IPOs as NSE Emerge or BSE SME when possible. SME IPOs need stronger caveats because lot values are higher, liquidity can be lower, data may be more fragmented, and market makers are part of the structure.

Required SME fields:

- Platform: NSE Emerge or BSE SME.
- Issue open date.
- Lot size.
- Minimum application amount.
- Market maker, if available.
- Registrar.

## SME Process Change From 2025-07-01

For SME IPOs opening on or after 2025-07-01, check official exchange circulars and the offer document before giving application-process guidance.

Expected new-process checks:

- Individual Investor minimum bid size is two lots with minimum application size above INR 2 lakh.
- Cut-off price bidding is not available for any category.
- Bid revision and cancellation rules are more restrictive than old SME retail bidding; verify the exact issue document or exchange circular before advising.
- Final-day timing can differ by platform, broker, category, or offer document.

For SME IPOs opening on or before 2025-06-30:

- Do not automatically apply the post-2025-07-01 process.
- State that old and new process transition handling may depend on the exchange and issue documents.

## Mainboard Difference

For mainboard IPOs:

- Retail application category typically applies up to INR 2 lakh.
- Cut-off bidding is normally available to eligible retail investors, subject to the offer document and broker flow.
- Still verify issue-specific rules before giving application instructions.
