# Source and Fallback Guide

## Official Source Order

Use official sources before aggregators or media:

1. SEBI public issue filings: draft offer documents, RHPs, final offer documents, observations, corrigenda, addenda, and other public issue documents.
2. NSE/BSE offer-document pages and issue information pages.
3. NSE Emerge and BSE SME issue pages for SME IPOs.
4. Issuer investor-relations or IPO pages.
5. BRLM or lead manager document mirrors.
6. Registrar, exchange notices, price band advertisements, basis-of-allotment notices, and other official public announcements.
7. Reputable secondary summaries only when official sources are unavailable or cannot be parsed.

## Official Regulatory Anchors

- SEBI circular `SEBI/HO/CFD/TPD1/CIR/P/2023/140`, dated 2023-08-09, reduced specified securities public issue listing timelines from T+6 to T+3 working days. T is issue closing date. It applied voluntarily for public issues opening on or after 2023-09-01 and became mandatory for public issues opening on or after 2023-12-01.
- NSE circular `NSE/IPO/68604`, dated 2025-06-18, describes the new SME IPO bidding process for issues opening on or after 2025-07-01. Relevant investor-facing checks include Individual Investor category, minimum two lots with application size above Rs 2 lakh, no cut-off price bidding, no downward modification/cancellation, final-day bidding close at 4:00 PM, and UPI mandate confirmation up to 5:00 PM.
- SEBI ICDR and current SEBI master circulars govern offer-document disclosure expectations. Use the latest available official version when citing current regulations.

## Document Selection

| Situation | Preferred document | Required caveat |
|---|---|---|
| IPO is only filed, not opened | DRHP or updated DRHP | Price band, dates, final issue size, and final allocations may be unavailable |
| IPO is open/upcoming with final terms | RHP | Final issue price may still be unavailable until pricing/allotment |
| IPO is completed | Prospectus/final offer document | Historical analysis; do not infer current subscription or price action without live sources |
| SME IPO with no SEBI PDF result | Exchange SME page, issuer page, BRLM page | Missing SEBI result does not mean no official document |
| PDF cannot be parsed | Abridged prospectus, AV disclosure, exchange metadata | Confidence no higher than Medium unless full official document data is still available |
| Only secondary summaries are available | Reputable IPO aggregators/news | Confidence Low; ask for official document URL |

## Confidence Labels

| Label | Use when |
|---|---|
| High | Full official DRHP/RHP/prospectus or official exchange document is parsed and key fields are cross-checked |
| Medium | Official abridged prospectus, AV disclosure, or exchange metadata is used, but the full PDF is inaccessible or partly unparsed |
| Low | Secondary summaries are used because official documents are unavailable |
| Unavailable | The field cannot be safely found or extracted |

## PDF Extraction Pitfalls

- Offer documents are long and table-heavy. Validate page context before extracting values.
- Scanned/image PDFs may require OCR; do not pretend table extraction was exact.
- Split rows, merged cells, notes, footnotes, and multiple currencies can corrupt totals.
- Cross-check offer size, fresh issue, OFS, objects amounts, and financial tables against the summary section, cover page, and exchange metadata.
- When values conflict, show both values, cite the source locations, and mark the field as needing manual review.

## Source Table Requirements

Every output must list:

- Source name.
- URL or document identifier.
- Source type: official document, official metadata, fallback official, or secondary.
- Document date or fetch date.
- What it was used for.
- Confidence.

