# IPO Application Rules

## ASBA And UPI ASBA

ASBA means Application Supported by Blocked Amount. The bank blocks the application amount in the applicant's account. If shares are allotted, the allotted value is debited; if not, the block is released. In ordinary ASBA language, "refund" often means lien release or unblocking, not money returning from the issuer.

UPI ASBA flow:

1. User submits bid details and UPI ID through broker, DP, RTA, syndicate member, or other eligible intermediary.
2. Intermediary uploads bid and UPI ID to the stock exchange bidding platform.
3. Exchange routes the details to the sponsor or escrow bank.
4. Sponsor bank triggers a UPI mandate.
5. User approves the mandate in the UPI app using UPI PIN.
6. Funds are blocked in the linked bank account.
7. After allotment, funds are debited for allotted shares or unblocked.

The application is incomplete until the mandate is approved and funds are blocked.

## Mainboard Categories

| Category | Amount | Cut-off? | Revision/cancellation |
|---|---:|---|---|
| Retail individual investor | Up to INR 2 lakh | Available in book-built IPOs | Can generally revise or withdraw while issue is open, subject to platform windows |
| sNII/sHNI | More than INR 2 lakh and up to INR 10 lakh | No | Cannot withdraw or lower bid size; upward revision may be platform-dependent |
| bNII/bHNI | More than INR 10 lakh | No | Cannot withdraw or lower bid size; bank ASBA is usually the practical route |
| QIB | Institutional | No | Not typical retail guidance |

NII portion split: one-third sNII, two-thirds bNII. Reservation categories such as employee, shareholder, or policyholder are issue-specific; verify eligibility, discount, maximum amount, and rules from the offer document.

## UPI Limit

Current UPI IPO mandate limit is INR 5 lakh per transaction. Do not describe this as "mainboard retail up to INR 5 lakh." Mainboard retail remains up to INR 2 lakh. Above INR 2 lakh, the application moves to NII/HNI or another eligible reservation category. Above INR 5 lakh, use bank ASBA.

## Cut-Off Vs Price Bidding

Cut-off means the user accepts the final issue price discovered through book-building. The block is calculated at the upper price band; excess is released if the final price is lower.

Use cut-off only when available:

- Mainboard book-built IPO.
- Retail or eligible reservation category where the offer document permits it.

Do not use cut-off for:

- NII/HNI or QIB.
- SME IPOs under the revised July 2025 SME process.
- Fixed-price issues.

If a retail mainboard bid is below the final issue price, it is not eligible for allotment.

## Lot And Amount Calculation

Always compute:

```text
application amount = lots x lot size x bid price
```

For cut-off bids, use the cap price. Check retail eligibility against cap-price amount, not floor-price amount. Quantity must be the minimum lot or a multiple of the lot size.

Example: price band INR 100-120, lot size 125, one lot at cut-off blocks `1 x 125 x INR 120 = INR 15,000`. Maximum mainboard retail lots are the highest whole number of lots not exceeding INR 2 lakh at cap price.

## SME IPOs Opening On Or After 2025-07-01

Apply revised SME process only after checking the issue open date. For SME IPOs opening on or after 2025-07-01:

- Existing Retail Individual Investor category is replaced by Individual Investor.
- Individual Investor applies for 2 lots with minimum application size above INR 2 lakh.
- Employee reserved category: minimum 2 lots above INR 2 lakh, multiples of lot size, not exceeding INR 5 lakh.
- Shareholder and policyholder categories: minimum 2 lots above INR 2 lakh.
- QIBs and NIIs apply for more than 2 lots.
- Cut-off bidding is unavailable to every category.
- Downward modification and cancellation are unavailable to every category.
- Last-day bidding closes at 4:00 PM.
- UPI mandate acceptance/confirmation remains available until 5:00 PM on the last bidding day.

For SME issues opening before 2025-07-01, verify the applicable process from the exchange circular, offer document, or broker/exchange issue page. Do not blindly apply the revised process.

## Current Post-Close Timeline

Default for current Indian equity public issues:

| Day | Expected milestone |
|---|---|
| T | Issue closes |
| T+1 working day | Basis of allotment finalization and initiation of refunds/unblocking are commonly scheduled |
| T+2 working day | Demat credit for allotted shares and continued unblock processing |
| T+3 working day | Listing and trading commencement |

T+3 became mandatory for public issues opening on or after 2023-12-01. State "working days" and check the issue schedule because market holidays shift dates. Mention T+6 only as historical context or if an older official document explicitly applies it.
