---
name: ipo-drhp-analyzer
description: Extracts and summarizes Indian IPO DRHP, RHP, and prospectus documents for retail-investor due diligence. Use when a user asks to analyze an IPO offer document, DRHP, RHP, prospectus, fresh issue/OFS split, objects of issue, promoters, risk factors, litigation, or SME offer-document disclosures.
---

# IPO DRHP Analyzer

## Read First

- `skills/shared/references/india_ipo_data_sources.md`
- `skills/shared/references/sme_vs_mainboard.md`
- `skills/ipo-drhp-analyzer/assets/output-template.md`
- `skills/ipo-drhp-analyzer/references/source-and-fallbacks.md`
- `skills/ipo-drhp-analyzer/references/drhp-section-map.md`
- `skills/ipo-drhp-analyzer/references/retail-interpretation.md`

## Core Rule

Be document-grounded. Analyze the official DRHP, RHP, prospectus, abridged prospectus, or exchange offer-document page before using summaries. If a field is not found, write `Unavailable` and explain the fallback instead of guessing.

## Workflow

1. Identify the IPO name, document URL if supplied, issue type, exchange/platform, and issue open date.
2. Classify the issue as mainboard, NSE Emerge, BSE SME, or unknown. If unknown, make classification a required source lookup.
3. Choose the best document:
   - Current/open IPO: prefer RHP over DRHP when available.
   - Completed IPO: prefer prospectus/final offer document.
   - Early-stage IPO: use DRHP and mark price/date fields as draft or unavailable.
   - SME IPO: search exchange/issuer/BRLM pages when SEBI pages do not show the document.
4. Use source hierarchy:
   - Official: SEBI public issue pages, NSE/BSE offer-document pages, official exchange SME pages, issuer site, BRLM site, registrar or public notices.
   - Fallback: abridged prospectus, AV disclosure, exchange metadata.
   - Last resort: reputable secondary summaries; label confidence `Low`.
   If an official PDF or SEBI page is found but cannot be fetched or parsed, run the retrieval failure fallback chain in `references/source-and-fallbacks.md` before concluding that the document is unavailable.
5. Extract only the sections needed for retail due diligence:
   - Source metadata and data freshness.
   - Business snapshot.
   - Offer structure with fresh issue vs OFS split.
   - Fresh issue objects and use of proceeds.
   - OFS and selling shareholders.
   - Promoters and group background.
   - Top risk factors.
   - Litigation and regulatory proceedings.
   - Financial snapshot.
   - Basis for issue price and KPIs.
   - Related-party transactions, auditor notes, capital structure, and SME-specific disclosures where relevant.
6. Apply current rules:
   - Default listing timeline is T+3 working days; T is issue closing date.
   - T+3 is mandatory for public issues opening on or after 2023-12-01.
   - Mention T+6 only as historical context or when analyzing an older issue.
   - For SME IPOs opening on or after 2025-07-01, check the revised SME process before giving action-oriented comments. Do not assume mainboard retail mechanics, cut-off bidding, or small lot sizes.
7. Produce the answer using `assets/output-template.md`.

## Required Interpretations

- Separate facts from retail implications.
- Fresh issue proceeds go to the issuer; OFS proceeds generally go to selling shareholders.
- Prominently flag OFS-dominant offers: 100%, above 75%, and above 50%.
- Do not treat DRHP valuation claims as an apply/avoid recommendation. Hand off detailed scoring to `ipo-financials-scorer` or final decisioning to `ipo-apply-advisor`.
- Do not guarantee allotment, listing gains, returns, GMP reliability, or regulatory outcomes.

## Missing Data Behavior

- If the PDF is inaccessible or table extraction is unreliable, use official exchange metadata, abridged prospectus, AV disclosure, issuer/BRLM pages, or ask for the exact document URL.
- List attempted official URLs and failure modes before relying on secondary summaries.
- If only secondary sources are available, state `Confidence: Low`, list missing official fields, and avoid firm conclusions.
- If the user asks for a decision, provide document risks and suggest running the apply-advisor workflow rather than giving personalized investment advice.
