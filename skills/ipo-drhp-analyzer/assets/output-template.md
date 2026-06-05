# [Company] IPO DRHP/RHP Analyzer

## Header

| Field | Value |
|---|---|
| IPO | [Company name] |
| Classification | Mainboard / NSE Emerge / BSE SME / Unknown |
| Issue open date | YYYY-MM-DD / Unavailable |
| Document used | DRHP / UDRHP / RHP / Prospectus / Abridged prospectus / AV disclosure / Exchange metadata / Secondary fallback |
| Document date | YYYY-MM-DD / Unavailable |
| Analysis date | YYYY-MM-DD |
| Confidence | High / Medium / Low |

## Source Checks

| Source | Type | Date checked | Used for | Confidence |
|---|---|---|---|---|
| [SEBI/NSE/BSE/issuer/BRLM/etc.] | Official document / Official metadata / Fallback official / Secondary | YYYY-MM-DD | [fields] | High / Medium / Low |

## Business Snapshot

| Field | Finding | Retail meaning |
|---|---|---|
| Business model |  |  |
| Revenue streams |  |  |
| Key dependencies |  |  |
| Claimed moat |  |  |

## Offer Structure

| Component | Amount | Shares | Percent of issue | Retail meaning |
|---|---:|---:|---:|---|
| Fresh issue |  |  |  | Funds the company after issue expenses |
| OFS |  |  |  | Proceeds generally go to selling shareholders |
| Total issue |  |  | 100% |  |

**OFS flag:** None / Caution above 50% / Exit-dominant above 75% / 100% OFS company receives no growth capital / Unavailable

## Fresh Issue Objects

| Object | Amount | Percent of fresh issue | Evidence | Retail interpretation |
|---|---:|---:|---|---|
|  |  |  |  |  |

## OFS and Selling Shareholders

| Selling shareholder | Type | Shares/amount sold | Percent of issue | Post-issue holding | Retail interpretation |
|---|---|---:|---:|---:|---|
|  | Promoter / Promoter group / Investor / Other |  |  |  |  |

## Promoters and Group Background

| Promoter/group | Background | Interests in issuer | Linked risks |
|---|---|---|---|
|  |  |  | OFS / RPT / Litigation / None found |

## Top Risk Factors

| Rank | Issuer wording summary | Category | Retail meaning |
|---:|---|---|---|
| 1 |  | Business / Financial / Regulatory / Governance / Litigation / External |  |

## Litigation and Regulatory Proceedings

| Party | Type | Forum/regulator | Amount | Status | Retail meaning |
|---|---|---|---:|---|---|
|  | Issuer / Subsidiary / Promoter / Director / Group company |  |  |  |  |

## Financial Snapshot

| Metric | FY-3 | FY-2 | FY-1 | Retail interpretation |
|---|---:|---:|---:|---|
| Revenue |  |  |  |  |
| PAT |  |  |  |  |
| Operating cash flow |  |  |  |  |
| Total debt |  |  |  |  |

## Basis for Issue Price and KPIs

| Item | Disclosure | Retail interpretation |
|---|---|---|
| EPS / P/E / RoNW / NAV |  |  |
| Peer comparison |  |  |
| KPIs / WACA / past transactions |  |  |

## Related-Party, Auditor, and Capital Structure Notes

| Area | Finding | Retail meaning |
|---|---|---|
| Related-party transactions |  |  |
| Auditor qualifications/restatements |  |  |
| Capital structure/dilution/lock-in |  |  |

## SME-Specific Checks

Use only if the issue is SME or classification is unknown.

| Check | Finding | Retail meaning |
|---|---|---|
| Platform | NSE Emerge / BSE SME / Unknown |  |
| Market maker |  |  |
| Lot size/minimum application |  |  |
| 2025-07-01 process applicability | Applies / Does not apply / Need issue open date |  |

## Missing Data and Caveats

- [Unavailable field]: [what was tried and what source or URL is needed]
- T+3 is the current default public issue listing timeline for applicable current IPOs; T+6 is historical unless the issue date/source proves otherwise.
- This is a document-risk summary, not personalized investment advice.

## Retail Investor Takeaways

| Takeaway | Why it matters | Follow-up |
|---|---|---|
|  |  | Run `ipo-financials-scorer` / `ipo-red-flags-detector` / `ipo-peer-comparison` / `ipo-apply-advisor` |

