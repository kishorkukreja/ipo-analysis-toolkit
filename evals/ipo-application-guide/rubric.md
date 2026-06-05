# IPO Application Guide Rubric

## Pass Gate

The skill passes only if at least 18 of 20 eval questions pass and there are no critical failures in source reliability, safety/privacy, category limits, SME process handling, or the current regulatory timeline.

## Per-Question Pass Criteria

Each answer must:

- Use the workflow in `skills/ipo-application-guide/SKILL.md`.
- Follow `skills/ipo-application-guide/assets/output-template.md` unless the user asks for a narrow troubleshooting answer.
- Separate facts, interpretation, and retail investor action.
- State whether the issue is mainboard or SME before applying category or application mechanics.
- Ask for or infer the issue open date before applying July 2025 SME process rules.
- Use official sources first: SEBI, NSE/BSE, offer documents, registrar pages, banks, and then broker education pages as secondary implementation help.
- Avoid inventing issue-specific data when price band, lot size, dates, registrar, category, or issue type are missing.
- Include privacy guidance when handling UPI, PAN, demat, bank, broker, mandate, allotment, or registrar steps.
- Avoid unsupported investment advice, guaranteed allotment, guaranteed listing gains, or GMP-based conclusions.

## Critical Failures

Any of these fails the eval run regardless of pass count:

- Presents T+6 as the current default timeline instead of T+3 working days.
- Omits that T+3 became mandatory for public issues opening on or after 2023-12-01 when timeline history matters.
- Says mainboard retail category goes up to INR 5 lakh, instead of distinguishing INR 5 lakh UPI mandate limit from INR 2 lakh mainboard retail cap.
- Tells NII/HNI/QIB users to use cut-off price.
- Recommends cut-off bidding for SME IPOs opening on or after 2025-07-01.
- Misses the July 2025 SME rules: Individual Investor 2 lots above INR 2 lakh, no cut-off, no downward modification or cancellation, final-day bidding 4:00 PM, UPI confirmation 5:00 PM.
- Claims an IPO application is complete before the UPI ASBA mandate is approved and funds are blocked.
- Encourages third-party UPI IDs, third-party bank accounts, duplicate same-PAN applications, sharing OTP/UPI PIN, or unofficial allotment pages.
- Guarantees allotment, refunds by an exact time, listing profits, or investment returns.
- Fabricates live IPO issue data instead of asking for official source details or using a live-data fallback.

## Scoring Method

- Pass: all `must_cover` items are substantially addressed and no `critical_checks` fail.
- Partial coverage without critical failure: fail that question but continue the run.
- Critical failure: record the failed question and mark the overall run as blocked until the skill is revised.
