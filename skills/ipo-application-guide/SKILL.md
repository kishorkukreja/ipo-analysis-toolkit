---
name: ipo-application-guide
description: Use when a user asks how to apply for an Indian IPO, approve an IPO UPI mandate, use ASBA, choose cut-off vs price bidding, revise or cancel a bid, troubleshoot allotment/refund/demat status, or compare mainboard and SME IPO application mechanics.
---

# IPO Application Guide

## Purpose

Guide Indian investors through the IPO application process for NSE/BSE mainboard and SME issues. This is operational guidance, not an apply/avoid recommendation.

## First Checks

Before giving instructions, establish:

- Issue type: mainboard, NSE Emerge, or BSE SME.
- Issue open date and close date.
- User category: retail, Individual Investor for SME, sNII, bNII, employee, shareholder, or policyholder.
- Route: broker/intermediary with UPI ASBA, or bank netbanking/mobile ASBA.
- Price band or fixed price, lot size, number of lots, registrar, and tentative schedule.

If any issue-specific data is missing, do not invent it. Ask for the RHP/prospectus, exchange page, broker issue page, or registrar name, and give only a provisional checklist.

## Required Output

Use `assets/output-template.md` for full guides. For narrow troubleshooting, keep the same section order in shorter form: facts, interpretation, action, safety.

Always include:

- Mainboard vs SME classification.
- Category and amount-limit check.
- Cut-off availability.
- Application amount calculation: `lots x lot size x bid price`; for cut-off, use the cap price.
- Mandate or ASBA block status.
- Current T+3 working-day post-close timeline where relevant.
- Official-source fallback and privacy block.

## Core Rules

Read `references/application-rules.md` when the answer involves category limits, cut-off, UPI limits, revision/cancellation, SME rules, or timelines.

Critical defaults:

- ASBA blocks money first; debit happens only if shares are allotted.
- UPI is a mandate mechanism layered on ASBA. A broker IPO bid is not complete until the user approves the UPI mandate and funds are blocked.
- Current UPI IPO mandate limit is INR 5 lakh per transaction, but mainboard retail category remains up to INR 2 lakh.
- Mainboard retail users can generally use cut-off in book-built IPOs. NII/HNI/QIB cannot use cut-off.
- SME IPOs opening on or after 2025-07-01 use the revised SME process: Individual Investor minimum 2 lots above INR 2 lakh, no cut-off, no downward modification or cancellation, final-day bidding closes 4:00 PM, UPI confirmation until 5:00 PM.
- Current default public issue timeline is T+3 working days from issue close. T+6 is historical unless an older issue or official document says otherwise.

## Workflows

Read `references/workflows-and-troubleshooting.md` for detailed broker UPI ASBA, bank ASBA, allotment, refund/unblock, demat credit, and mistake-handling flows.

Route selection:

- Use broker/intermediary UPI ASBA for typical eligible individual applications within UPI support and mandate limits.
- Prefer bank ASBA for applications above INR 5 lakh, bNII applications, repeated UPI mandate failures, unsupported broker categories, or users who want a direct bank block.
- For mainboard NII/HNI or SME, warn before submission that cancellation or reduction may not be available.

## Source And Safety Discipline

Read `references/sources-and-privacy.md` when sources, live data, registrar links, or user-sensitive details are involved.

Also reuse shared plugin references when relevant: `skills/shared/references/india_ipo_data_sources.md`, `skills/shared/references/sme_vs_mainboard.md`, and `skills/shared/references/registrars.md`.

Use official sources first: SEBI, NSE/BSE, RHP/prospectus, issuer/BRLM notices, registrars, SCSB banks. Use broker education pages only for implementation labels and app-specific behavior. Use IPO aggregators only as secondary context.

Never ask for or expose UPI PIN, OTP, full bank login details, broker password/PIN, full demat login, or unnecessary PAN/account data. Tell users to use their own UPI ID and bank account; third-party UPI IDs or bank accounts are rejection risks.

## Refusals And Boundaries

Do not guarantee allotment, refunds by an exact hour, listing gains, or investment returns. If the user asks whether they should apply, redirect to process guidance or recommend using `ipo-apply-advisor` for a separate decision framework.
