# DRHP Section Map

Section names vary by issuer. Use this map to find equivalent sections.

## P0 Extractions

| Area | Common labels | Extract |
|---|---|---|
| Source metadata | Cover page, summary, definitions, disclaimers | Company name, document type, document date, exchanges, BRLMs, registrar, face value, issue type |
| Offer structure | The Offer, Offer Structure, Issue Details | Fresh issue amount/shares, OFS amount/shares, total issue, selling shareholders, reservations, QIB/NII/Individual/RII split |
| Objects | Objects of the Offer, Objects of the Issue | Use of fresh issue proceeds, amount, percentage of fresh issue, schedule, implementation status, GCP amount |
| Risk factors | Risk Factors | Top internal risks in order, external risks, repeated themes, retail meaning |
| Promoters | Our Promoters and Promoter Group, Group Companies | Promoter names, background, experience, interests, post-issue holding, disqualifications if disclosed |
| Litigation | Outstanding Litigation and Material Developments | Cases by/against issuer, subsidiaries, promoters, directors, group companies; forum, amount, status, risk type |
| Financials | Restated Financial Information, Auditor's Report, MD&A | Revenue, EBITDA/PAT where available, debt, operating cash flow, margins, fiscal years, qualifications |

## P1 Extractions

| Area | Common labels | Extract |
|---|---|---|
| Basis for price | Basis for Offer Price, Basis for Issue Price | EPS, P/E, RoNW, NAV, peer comparison, KPIs, WACA, past transactions, price justification |
| Related parties | Related Party Transactions, notes to financials | Counterparties, amount, balances, loans/guarantees, revenue or asset concentration |
| Capital structure | Capital Structure, Shareholding Pattern | Pre/post capital, promoter holding, pledge, ESOPs/options/convertibles, dilution and lock-in |
| Auditor matters | Auditor's Report, Restated Financials, Other Financial Information | Qualifications, emphasis of matter, restatement adjustments, auditor changes |
| Material contracts | Material Contracts and Documents for Inspection | Contracts tied to objects, loans, leases, licenses, underwriting, registrar, market making |

## SME-Specific Fields

For NSE Emerge or BSE SME IPOs, also extract:

- Market maker name, reservation, and market making arrangement.
- Lot size and minimum application amount when disclosed.
- Platform and trading/settlement restrictions.
- Liquidity and spread risk disclosures.
- Issue opening date, because process guidance changes for issues opening on or after 2025-07-01.

## Fresh Issue vs OFS Calculations

Use amounts when available; otherwise use shares. Never mix amount and share denominators in the same percentage.

```text
total_issue = fresh_issue + OFS
fresh_pct = fresh_issue / total_issue
ofs_pct = OFS / total_issue
promoter_ofs_pct = promoter_selling_shareholder_OFS / total_issue
```

Flagging heuristic:

| OFS level | Retail interpretation |
|---|---|
| 100% OFS | Company receives no growth capital from the IPO |
| OFS above 75% | Exit-dominant offer; promoter or investor sale must be prominent |
| OFS above 50% | Caution; evaluate promoter retention, reasons for sale, and fresh issue objects |
| Promoter OFS | Link to promoter background, post-issue holding, and litigation/RPT context |
| Investor/VC/PE OFS | Explain as financial investor exit; still check valuation and remaining stake |

## Objects of Issue Checks

Only fresh issue proceeds fund objects. Do not say OFS proceeds are used for company purposes.

Check:

- Debt repayment amount and lender names where disclosed.
- Working capital assumptions and period covered.
- Capex details, locations, contracts, supplier quotes, and implementation schedule.
- Acquisitions or investments and whether targets are identified.
- General corporate purposes and whether caps apply.
- Issue expenses and whether they reduce net proceeds.

## Risk Factor Handling

- Preserve the issuer's risk ordering where practical; early risks are often considered more material.
- Group risks by business, financial, regulatory, governance, litigation, customer/supplier concentration, and external risks.
- Write both `issuer wording summary` and `retail meaning`.
- Do not dilute risk factors into generic language; keep specific dependencies, amounts, percentages, and counterparties when available.

