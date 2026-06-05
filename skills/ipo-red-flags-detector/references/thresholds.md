# Red-Flag Thresholds

Use these thresholds as investor-risk heuristics unless current SEBI, NSE, BSE, or offer-document evidence gives a stricter rule.

## Offer Structure and Objects

| Signal | Severity |
|---|---|
| Mainboard OFS 20-40% of issue | Minor |
| Mainboard OFS 40-60% | Major |
| Mainboard OFS 60-75% | Major+ |
| Mainboard OFS > 75% or 100% OFS | Critical |
| Growth story but low fresh capital or uncosted objects | Major |
| GCP > 15% of fresh issue | Major, or Critical if paired with RPTs/weak OCF |
| Mainboard repayment to promoter/group/related-party lender | Major governance flag |
| SME repayment to promoter/promoter group/related-party lender | Auto-reject if current platform rules apply |

OFS can be a false positive for mature, cash-generative, low-debt issuers or government/sponsor divestments. Do not auto-reject on OFS alone unless other accounting, governance, or source-quality flags support it.

## Cash Flow and Earnings Quality

| Signal | Severity |
|---|---|
| OCF/PAT >= 0.8 | Clean |
| OCF/PAT 0.5-0.8 | Minor |
| OCF/PAT 0-0.5 | Major |
| Positive PAT with negative OCF in latest year | Major |
| Positive PAT with negative OCF in 2 of last 3 years | Auto-reject unless sector mechanics are clearly supported |
| SME EBITDA positive but FCFE negative in 2 of 3 years | Major/Critical |
| Receivables growth > revenue growth by 50%+ for 1 year | Minor/Major |
| Receivables growth > 2x revenue growth for 2 years | Major |
| Debtor days > 120 and worsening without sector explanation | Major |
| Receivables dominate assets and OCF is weak | Critical |
| PAT or EBITDA > 3x in IPO year | Critical for SME, Major for mainboard |
| Margin expansion > 500 bps in latest year without explanation | Major |

Acceptable explanations may include NBFC/lender growth, seasonal inventory, infrastructure ramp-up, contracted inventory build, export incentives, or high-growth receivables, but only when disclosed and independently supported.

## Auditor and Restatement

| Signal | Severity |
|---|---|
| Emphasis of matter on litigation, going concern, or receivables | Major |
| Qualified opinion affecting revenue, receivables, inventory, loans, or going concern | Critical |
| Disclaimer or adverse opinion | Auto-reject |
| Auditor unable to verify bank balances, debtors, inventory, or RPT balances | Critical |
| Auditor changed within 24 months of DRHP without clear reason | Major |
| Auditor tenure under 2 years plus weak cash/RPT evidence | Critical composite flag |
| Restatement changes PAT, revenue, or net worth by 1-5% | Minor |
| Restatement changes PAT, revenue, or net worth by 5-10% | Major |
| Restatement changes PAT, revenue, or net worth by > 10% | Critical |
| Loss becomes profit or profit becomes loss after restatement | Critical |

IPO restated financials are normal. The red flag is material restatement, unexplained auditor change, weak auditor evidence, or restatement tied to revenue, RPTs, receivables, inventory, loans, or promoter balances.

## Promoter and Governance

| Promoter pledge or encumbrance | Severity |
|---|---|
| 0% | Clean |
| 1-10% | Info/Minor |
| 10-25% | Minor |
| 25-50% | Major |
| 50-75% | Critical |
| > 75% | Auto-reject |

Escalate pledge risk if it secures promoter/group debt, was created shortly before IPO, uses opaque lenders, affects locked-in shares, or appears with defaults/litigation.

Auto-reject or Critical for active debarment, wilful default, fraudulent borrower status, fugitive economic offender status, or active SEBI/ED/SFIO/PMLA-type action involving fraud, fund diversion, market manipulation, or financial misstatement.

## Related-Party Transactions

| Signal | Severity |
|---|---|
| RPT sales or purchases 5-10% | Minor |
| RPT sales or purchases 10-20% | Major |
| RPT sales or purchases > 20% | Critical |
| RPT loans/advances to promoters/group > 5% net worth | Major |
| RPT loans/advances > 10% net worth | Auto-reject unless strong arms-length evidence |
| RPTs > 30% of revenue or purchases | Auto-reject unless strongly explained |
| Circular flow among issuer, group entity, customer, or vendor | Critical |
| Promoter/group entity is both major customer and major supplier | Critical |

Distinguish ordinary disclosed RPTs from value-transfer risk. Core questions: pricing basis, cash settlement, recurrence, board/audit approval, and whether RPTs explain profit growth.

## Litigation and Regulatory Actions

| Signal | Severity |
|---|---|
| Routine tax/GST matters < 2% net worth | Minor |
| Civil/commercial dispute 2-10% net worth | Major if operationally material |
| Contingent liabilities > 10% net worth | Major |
| Tax/regulatory demands > 25% net worth | Critical |
| Criminal proceeding against promoter/director | Major/Critical |
| SEBI/exchange penalty for disclosure failure | Major |
| SEBI order involving fraud, diversion, manipulation, or misstatement | Auto-reject |
| ED/PMLA/SFIO involvement with issuer/promoter | Auto-reject unless stale and resolved |
| IBC admission or admitted winding-up petition | Auto-reject/eligibility concern |

Report unquantified litigation as a data gap. Compare risk factors with the litigation section for consistency.

## Business Model and Concentration

| Signal | Severity |
|---|---|
| Top customer 20-25% revenue | Minor |
| Top customer 25-40% revenue | Major |
| Top customer > 40% revenue | Critical for SME, Major/Critical for mainboard |
| Top 5 customers > 70% revenue | Major |
| Top customer is related party | Critical |
| Top supplier > 40% purchases | Major/Critical |
| License pending, expiring, or under litigation for core business | Critical |
| Cash runway after IPO below 12 months for loss-making company | Major/Critical |

## Composite Critical Rules

Escalate to Critical when any 3 of these appear: OFS > 60% mainboard or meaningful promoter OFS in SME, GCP > 15% or at SME cap, auditor tenure < 2 years, revenue/PAT spike > 100%, OCF/PAT < 0.5, receivables growth > 2x revenue growth, RPTs 10-20%, top customer > 40%, valuation > 2x peer median, weak merchant banker, unclear SME market maker, material litigation > 10% net worth.
