---
name: ipo-calendar
description: Use this skill for Indian IPO calendar requests covering NSE/BSE mainboard IPOs, NSE Emerge IPOs, and BSE SME IPOs. Trigger when the user asks what IPOs are open, upcoming, recently closed, awaiting allotment/listing, recently listed, filed with SEBI/exchanges, or asks for IPO dates, price bands, lot size, issue size, registrar, DRHP/RHP/prospectus links, listing dates, or SME versus mainboard classification.
---

# IPO Calendar

Use this skill to build a live Indian IPO calendar for retail investors. Do not rely on a static local calendar; IPO status, dates, price bands, issue size, registrar links, and listing dates change frequently.

## Before You Answer

Read the relevant references when needed:

- `skills/shared/references/india_ipo_data_sources.md` for repo-wide source hierarchy.
- `skills/shared/references/sme_vs_mainboard.md` when classifying or explaining SME issues.
- `skills/shared/references/registrars.md` when naming or linking registrars.
- `skills/ipo-calendar/references/source-hierarchy.md` for calendar-specific source ranking and caveats.
- `skills/ipo-calendar/references/calendar-fields.md` for required fields and status normalization.
- `skills/ipo-calendar/references/timeline-and-sme-rules.md` for T+3 timeline and SME process branching.
- `skills/ipo-calendar/assets/output-template.md` for the required response shape.

## Workflow

1. Identify the request scope:
   - Market: mainboard, SME, or both. Default to both if the user does not specify.
   - Status: open, upcoming, closed but not listed, recently listed, filed/pipeline, or all active statuses.
   - Date window: use the user's dates if supplied; otherwise use a near-term window that fits the request and state it clearly.

2. Fetch live data:
   - Prefer official SEBI, NSE, BSE, registrar, issuer, and BRLM sources for dates, status, documents, platform, registrar, and listing details.
   - Use reputable IPO aggregators only to fill gaps, cross-check retail-friendly fields, or summarize when official pages are inaccessible.
   - Search the web when current IPO facts are needed. Include source timestamps or access dates for volatile fields.

3. Classify every issue:
   - Mainboard, NSE Emerge, BSE SME, or unknown.
   - If classification is unknown, mark it as a required lookup rather than guessing.
   - Separate mainboard and SME issues in the output unless the user explicitly asks for a single combined table.

4. Normalize statuses:
   - Use the normalized statuses in `references/calendar-fields.md`.
   - Preserve the raw official status in notes when it differs from the normalized status.
   - Do not call a filed-stage company an "upcoming IPO" unless official dates or price-band notices exist.

5. Handle timelines:
   - Current default public issue timeline is T+3 working days from issue close, where T is the issue closing date.
   - Use official allotment, refund, demat credit, and listing dates when available.
   - If computing dates from the close date, label them as "expected" and mention that exchange, registrar, holiday, or issue-extension updates can change them.
   - Do not present T+6 as the current default. Mention T+6 only for historical issues or stale source correction.

6. Apply SME-specific handling:
   - Always show SME platform, lot size, and minimum application amount when available.
   - For SME IPOs opening on or after 2025-07-01, check the new process rules before giving application guidance: minimum two lots for Individual Investors with application amount above INR 2 lakh, no cut-off price bidding, and process-specific bid revision/cancellation constraints.
   - For SME IPOs opening on or before 2025-06-30, do not apply the new process automatically; state that transition handling may depend on the exchange and offer document.

7. Report missing data safely:
   - Use "Not found in checked sources" rather than inventing fields.
   - Name the source checked and ask for the exact exchange page, offer document, or registrar link if the missing field is needed to continue.
   - If official and secondary sources conflict, prefer official data and call out the conflict.

8. Keep investment boundaries:
   - This skill reports calendar facts and practical caveats. It does not decide whether the user should apply.
   - Do not promise allotment, listing gains, GMP-based returns, or guaranteed timelines.
   - If the user asks whether to apply, provide calendar facts briefly and route the decision analysis to `ipo-apply-advisor`.

## Output Requirements

Use `assets/output-template.md`. Every complete calendar answer must include:

- Scope and data freshness.
- Source priority used.
- Separate mainboard and SME sections, or a clear reason if one section has no results.
- Calendar rows with status, dates, price band or issue price, lot size, minimum amount, issue size, platform, registrar, documents, and notes where available.
- A T+3 timeline section for closed/open issues when listing-related dates matter.
- Missing data and conflicts.
- Retail investor caveats and next actions.
