# Extraction and Source Rules

## Source Hierarchy

Use sources in this order:

1. SEBI DRHP/RHP/prospectus PDF or exchange-hosted offer document.
2. Draft abridged prospectus for navigation and summary cross-check.
3. NSE/BSE issue pages and SME eligibility/platform pages for classification and market context.
4. Company IPO or investor page when it links the same official documents.
5. Rating agency reports for sector benchmarks, not as primary issuer scoring evidence.
6. Brokerage or IPO-review summaries only when primary documents are inaccessible.
7. News only for current regulatory action or material developments, with citation.

If the user supplies a DRHP/RHP/prospectus URL, use it before searching.

## Offer Document Sections

Read these in priority order:

1. Summary of Restated Consolidated Financial Information.
2. Restated Consolidated Financial Information or Financial Information.
3. Management's Discussion and Analysis.
4. Basis for Issue Price.
5. Capitalisation Statement.
6. Objects of the Issue, especially debt repayment or working capital funding.
7. Risk Factors.
8. Outstanding Litigation and Material Developments.
9. Related Party Transactions.
10. Our Business for operating KPIs and segment metrics.

## Minimum Extraction Fields

| Field | Preferred source | Notes |
|---|---|---|
| Revenue from operations | Restated P&L | Exclude other income unless clearly operating. |
| Total income | Restated P&L | Context only; do not use for revenue CAGR. |
| EBITDA | Reported KPI or computed | If computed, disclose formula. |
| EBIT | Computed | PBT plus finance cost, or EBITDA less depreciation. |
| PAT/restated profit | Restated P&L | Use PAT attributable to owners when minority interest is material. |
| Net worth/equity | Balance sheet | Record issuer definition. |
| Borrowings | Balance sheet | Include current and non-current borrowings. |
| Cash and equivalents | Balance sheet | Include bank balances only when definition supports it. |
| Finance cost | P&L | Needed for interest cover. |
| Depreciation and amortisation | P&L | Needed for EBITDA/EBIT bridge. |
| CFO | Cash flow statement | Use net cash from operating activities. |
| Capex | Investing cash flow/notes | Prefer purchase of PPE and intangibles. |
| Trade receivables | Balance sheet | Use average balances for days metrics. |
| Inventory | Balance sheet | Not applicable to many services, SaaS, banks, and NBFCs. |
| Trade payables | Balance sheet | Use average balances for DPO. |
| COGS or cost of materials | P&L | Use proxy only when defensible and label it. |
| Contingent liabilities | Notes | Use as override/context when material. |
| Related-party transactions | Notes | Flag if material to revenue, costs, loans, assets, or guarantees. |
| Auditor qualifications | Auditor report | Critical if affecting revenue, profit, assets, debt, cash flow, or going concern. |

## Period and Unit Controls

- Use restated consolidated financial statements first.
- Use Indian fiscal years ending March 31 unless the issuer discloses another year-end.
- Display FY2025 as year ended 2025-03-31.
- Keep stub periods separate, for example `9M FY2026`.
- Annualize revenue and flow items only when necessary, defensible, and clearly flagged.
- Do not annualize working-capital balance-sheet items.
- Normalize units consistently, preferably Rs crore.
- Preserve sign conventions; parentheses usually mean negative values.
- Avoid ratios from mismatched periods.
- For average balance-sheet ratios, use beginning and ending balances for the same fiscal year.
- Do not use post-issue equity for historical ROE unless computing a separate pro-forma dilution view.

## KPI Disclosure Handling

- Extract issuer-disclosed KPIs and definitions.
- Label each KPI as `reported_by_issuer`, `computed_by_skill`, or `both`.
- If issuer and skill formulas differ, show both and explain the difference.
- Capture whether KPI definitions were audit-committee approved and professionally certified when disclosed.
- Do not infer omitted pre-IPO investor KPIs unless the offer document states the omission.

## DRHP Extraction Fallback

When PDF extraction fails:

1. Try the summary financial table and restated financial statement pages separately.
2. Use the draft abridged prospectus to locate page references, then cross-check the full document.
3. Try exchange-hosted versions or issuer/BRLM-hosted copies.
4. Use secondary summaries only for provisional output; mark `Financial source: secondary fallback` and confidence `Low`.
5. Ask the user for the exact document URL if primary financials remain unavailable.
