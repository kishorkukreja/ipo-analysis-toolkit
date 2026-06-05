# IPO Calendar Fields

## Normalized Statuses

Use these statuses in calendar outputs:

| Status | Meaning |
|---|---|
| Open | Bidding is currently open. |
| Upcoming | Dates or price band are officially announced but bidding has not opened. |
| Closing today | Bidding is open and the issue closes today. |
| Closed - allotment pending | Bidding closed and basis of allotment is not finalized or not found. |
| Closed - listing pending | Allotment/demat/refund events are complete or scheduled and listing is pending. |
| Recently listed | Listing occurred within the requested or default lookback window. |
| Filed / under process | DRHP, exchange filing, or in-principle process exists, but IPO dates are not announced. |
| Withdrawn / returned | Official source says the filing or issue was withdrawn, returned, or not proceeding. |
| Unknown | Status cannot be verified from checked sources. |

Preserve the official raw status in notes when it differs from the normalized status.

## Required Fields

Include these fields when available:

- Company.
- Status.
- Segment: mainboard, NSE Emerge, BSE SME, or unknown.
- Platform or exchange.
- Issue open date.
- Issue close date.
- Basis of allotment date.
- Refund or UPI unblock date.
- Demat credit date.
- Listing date.
- Price band or fixed issue price.
- Lot size.
- Minimum application amount.
- Issue size.
- Fresh issue and OFS split, if available.
- Registrar.
- DRHP/RHP/prospectus link.
- Official exchange page or source link.
- Notes and caveats.

## Optional Fields

Include these only when reliable:

- Anchor investor date.
- Market maker name and reservation for SME IPOs.
- BRLM or merchant banker.
- Face value.
- Issue type: book-built, fixed price, OFS, FPO, rights, debt, InvIT, REIT, or other.
- Subscription snapshot, only with timestamp and source.

## Filtering

For normal IPO calendar requests:

- Include equity IPOs on NSE/BSE mainboard, NSE Emerge, and BSE SME.
- Exclude rights issues, debt public issues, InvITs, REITs, SM-REITs, buybacks, and OFS-only secondary-market offers unless the user asks for those instruments.
- Do not mix foreign IPOs into the Indian IPO calendar unless explicitly requested.
