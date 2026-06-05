---
name: ipo-allotment-checker
description: Find official Indian IPO allotment-status routes, explain registrar/BSE/NSE checks, and troubleshoot refunds, UPI mandate release, demat credit, and rejected or missing records. Use when the user asks to check IPO allotment, registrar status, PAN/application/DP lookup steps, refund unblock, mandate release, demat credit, basis of allotment, or why an IPO application was not allotted.
---

# IPO Allotment Checker

## Core Workflow

1. Identify the IPO, issue type, exchange/platform, issue closing date, and registrar from the RHP/prospectus, SEBI/exchange page, or a reliable IPO calendar.
2. Use the official registrar allotment-status page first. Use BSE/NSE only as fallbacks or cross-checks.
3. Do not ask the user to paste PAN, application number, DP/client ID, bank account, IFSC, or screenshots into chat. Tell them to enter identifiers only on official HTTPS registrar/exchange pages.
4. Apply the current T+3 public issue framework by default. Treat T+6 as historical unless the IPO predates the transition or an official source says otherwise.
5. Explain the result and next action: allotted, not allotted, partial allotment, pending, record not found, rejected/technical rejection, delayed refund/unblock, or missing demat credit.
6. Use the output structure in [assets/output-template.md](assets/output-template.md).

## What To Read

- For official registrar URLs, lookup inputs, and fallback routes, read [references/registrar-lookup.md](references/registrar-lookup.md).
- For T+3 refund, unblock, demat credit, listing, and SME process handling, read [references/timeline-and-sme.md](references/timeline-and-sme.md).
- For status interpretation, privacy, phishing warnings, and escalation, read [references/troubleshooting-and-safety.md](references/troubleshooting-and-safety.md).
- Shared source hierarchy is in `skills/shared/references/india_ipo_data_sources.md`; shared registrar basics are in `skills/shared/references/registrars.md`.

## Response Rules

- If the user gives only an IPO name, find or ask for the registrar before giving lookup steps. Do not request PAN.
- If live/current IPO facts are needed, browse current official sources where available. If browsing is unavailable or data cannot be found, state what is missing and ask for the exact RHP, exchange, or registrar URL.
- Include mainboard/SME classification. For SME IPOs, include platform and higher-lot/liquidity caveats; for SME issues opening on or after 2025-07-01, use "Individual Investor" framing and note that cut-off bidding is not available.
- For refund/unblock questions, calculate the user's position in the T+3 working-day cycle when closing date is known. If before T+2/T+3, say it may still be within the normal window.
- Never guarantee allotment, refund timing, listing price, or investment returns. Do not provide listing-day sell/hold advice.
- Warn against unofficial status pages or callers claiming paid allotment help.

## Minimum Output

Every complete answer should include:

- IPO identity and classification.
- Data freshness and missing data.
- Official status-check route with registrar first and BSE/NSE fallbacks.
- Details the user may need, minimized to PAN/application number/DP-client ID options without asking them to paste values.
- Interpretation and next steps.
- Refund, UPI mandate release, and demat-credit timeline under T+3.
- Safety caveats and sources.
