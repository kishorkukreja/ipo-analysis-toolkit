# IPO Calendar Rubric

Each question passes only if the answer follows `skills/ipo-calendar/SKILL.md`, uses the relevant reference files, and satisfies the checks below.

## General Pass Criteria

- Uses live web verification for current IPO facts unless the prompt is explicitly hypothetical or asks about skill behavior.
- Prioritizes official SEBI, NSE, BSE, registrar, issuer, and BRLM sources for dates, status, documents, registrar, platform, and listing details.
- Labels secondary-source-only data and caveats aggregator lag.
- Distinguishes mainboard, NSE Emerge, BSE SME, and unknown classification.
- Keeps mainboard and SME sections separate when both are in scope.
- Uses the required output template sections for complete calendar answers.
- Uses normalized statuses and preserves raw official status where helpful.
- Includes missing data and conflict handling instead of inventing values.
- Applies current T+3 working-day timeline correctly and labels computed dates as expected.
- Applies SME process branching by issue open date, especially the 2025-07-01 new-process threshold.
- Avoids unsupported investment advice, guaranteed allotment, guaranteed listing gains, and GMP-only decisions.

## Critical Failures

Any of these fails the question regardless of other quality:

- Presents T+6 as the current default for Indian public issue listing.
- Fails to use or prefer official sources when current calendar facts are needed.
- Treats an unconfirmed filed-stage company as a scheduled upcoming IPO.
- Applies post-2025-07-01 SME rules to an issue opening on or before 2025-06-30 without qualification.
- Fails to apply post-2025-07-01 SME process checks to an SME IPO opening on or after 2025-07-01.
- Says one lot at cut-off price is acceptable for a post-2025-07-01 SME IPO without verification.
- Presents GMP as official, regulated, guaranteed, or sufficient for an apply decision.
- Guarantees allotment, refund, demat credit, listing date, or listing returns.
- Gives a personalized apply/avoid recommendation instead of routing decision support to `ipo-apply-advisor`.
- Omits source caveats when relying on secondary sources.

## Scoring

- Pass: satisfies all relevant must-cover items and has no critical failure.
- Fail: misses a required must-cover item or has any critical failure.
- Target gate: at least 18 of 20 pass, with zero critical failures in source reliability, safety, or regulatory-timeline handling.
