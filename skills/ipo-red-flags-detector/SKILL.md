---
name: ipo-red-flags-detector
description: Detects document-backed red flags in Indian NSE/BSE mainboard and SME IPOs for retail-investor risk review. Use when a user asks whether an IPO has warning signs, governance issues, weak cash conversion, risky OFS/objects, SME liquidity risks, litigation, auditor concerns, related-party issues, or an apply/avoid risk scan.
---

# IPO Red Flags Detector

## Scope

Use this skill only for Indian IPOs on NSE/BSE mainboard, NSE Emerge, and BSE SME. It is a forensic warning-sign scan, not a full recommendation engine. Separate facts, interpretation, and retail-investor action, and never promise returns, allotment, listing gains, or safety.

## Quick Workflow

1. Identify the IPO, issue type, platform, issue-open date, document version, and source URLs.
2. If issue type or issue-open date is unknown, state the gap. For SME process-specific conclusions, ask for or verify the open date before applying post-2025-07-01 rules.
3. Use sources in this order: current DRHP/RHP/prospectus/abridged prospectus, SEBI and exchange sources, registrar/exchange issue pages, issuer filings, then reputable secondary sources only as caveated support.
4. Scan the required DRHP/RHP areas: issue details, risk factors, objects, capital structure, restated financials, MD&A, RPTs, litigation, promoters/group companies, basis for issue price, and abridged prospectus.
5. Apply the red-flag thresholds in [thresholds.md](references/thresholds.md). For SME IPOs, also apply [sme-rules-and-liquidity.md](references/sme-rules-and-liquidity.md).
6. For every flag, provide evidence, source section/page or URL, metric, threshold, severity, confidence, why it matters, and what would reduce the concern.
7. Use [output-template.md](assets/output-template.md) for the final answer.

## Required Scan Areas

Always cover these domains, even if the result is a clean check or missing data:

- Offer structure: OFS, fresh issue, selling shareholder identity, use of proceeds, GCP, debt repayment, promoter or related-party loan repayment.
- Cash quality: OCF/PAT, OCF/EBITDA, FCFE where available, receivables, inventory, sudden pre-IPO margin or PAT spike.
- Governance: promoter pledge or encumbrance, promoter exit pattern, group-company history, related-party transactions, loans, advances, guarantees, asset transfers.
- Legal and regulatory: issuer/promoter/director litigation, SEBI/exchange actions, criminal/economic-offence disclosures, IBC/winding-up, contingent liabilities.
- Audit quality: auditor qualifications, emphasis of matter, adverse/disclaimer opinions, auditor change within 24 months, material restatements.
- Business model: customer/supplier concentration, license dependence, aggressive adjusted metrics, revenue/asset mismatch.
- SME-specific: platform, open date, eligibility/process caveats, market maker, merchant banker, free float, lot-size and liquidity risk, market-making obligation limits.
- Data quality: missing DRHP/RHP sections, inaccessible PDFs, stale sources, secondary-source-only facts.

## Severity Model

Use a hybrid model:

```text
Critical = 5 points
Major = 3 points
Minor = 1 point
Info = 0 points
SME multiplier = +25% score or one severity uplift for accounting, governance, and liquidity flags
Data gap penalty = +1 to +3 points for missing core sections, inaccessible documents, or unquantified amounts
```

Rating bands:

| Score | Rating | Suggested stance |
|---:|---|---|
| 0-2 | Low | Proceed only after normal IPO diligence |
| 3-6 | Moderate | Caution |
| 7-11 | High | Strong caution |
| 12+ | Severe | Avoid unless exceptional counter-evidence exists |
| Any auto-reject | Avoid | Do not soften with GMP or subscription |

## Hard Safety Rules

- Do not treat GMP, subscription, anchor demand, or social sentiment as official or sufficient for an apply decision.
- Do not describe T+6 as the current IPO timeline. Use T+3 as the current default unless the issue is historical or official documents say otherwise.
- Do not issue a strong clean result without DRHP/RHP or equivalent official offer-document evidence.
- Do not defame auditors, bankers, promoters, or issuers. State document-backed risks and confidence levels.
- Do not apply SME process-specific post-2025-07-01 guidance without checking the issue-open date.
- When evidence is unavailable, say what is missing, what provisional sources were used, and what document would resolve the gap.

