# IPO Calendar Source Hierarchy

Use this hierarchy for live Indian IPO calendar data.

## Official Sources

1. SEBI public issue filings
   - URL: https://www.sebi.gov.in/filings/public-issues.html
   - Best for DRHP, RHP, final prospectus, observations, and filed-stage validation.
   - Do not treat a SEBI filing alone as a scheduled IPO unless official dates are available.

2. SEBI T+3 public issue timeline circular
   - URL: https://www.sebi.gov.in/legal/circulars/aug-2023/reduction-of-timeline-for-listing-of-shares-in-public-issue-from-existing-t-6-days-to-t-3-days_75122.html
   - Circular: SEBI/HO/CFD/TPD1/CIR/P/2023/140 dated 2023-08-09.
   - Use as the current official timeline anchor for public issue listing from T+6 to T+3 working days.

3. NSE current/upcoming/past IPO pages
   - URL: https://www.nseindia.com/market-data/all-upcoming-issues-ipo
   - Best for NSE current, upcoming, past issue status and subscription snapshots.
   - Dynamic pages may require search-result snippets, CSV downloads, or secondary cross-checks.

4. NSE corporate filings offer documents
   - URL: https://www.nseindia.com/companies-listing/corporate-filings-offer-documents
   - Best for offer documents, issue composition, price band, market lot, registrar, market maker, listing platform, and listing date where available.

5. BSE live public issues
   - URL: https://www.bseindia.com/markets/PublicIssues/IPOIssues_new.aspx?Type=p&id=1
   - Best for BSE public issue status, start/end dates, offer price, and issue type.
   - Filter out rights issues, debt, InvITs, REITs, SM-REITs, and other non-equity issues unless the user asks for them.

6. BSE IPO process status
   - URL: https://www.bseindia.com/markets/PublicIssues/IPOProcess_Status.aspx
   - Best for filed-stage and approval-stage BSE pipeline issues.
   - Use statuses such as under process, clarification sought, in-principle approval issued, withdrawn, or returned.

7. Exchange SME circulars
   - NSE circular Ref No. NSE/IPO/68604 dated 2025-06-18 is the official source for the new SME IPO bidding process effective for SME IPOs opening on or after 2025-07-01.
   - Use exchange circulars or offer documents before broker summaries for SME process details.

8. Registrar, issuer, and BRLM pages
   - Use for registrar identity, allotment status page, basis of allotment notice, refund/unblocking dates, and issue documents.

## Secondary Sources

Use Chittorgarh, InvestorGain, IPOWatch, Moneycontrol, Economic Times, and broker education pages when official sources are unavailable, dynamic, or missing retail-friendly fields.

Secondary sources can help with:

- Consolidated open/upcoming/recently listed views.
- Lot value and retail application amount.
- Registrar links.
- Issue-size summaries.
- IPO status notes.

Always label secondary-source-only fields. Aggregator calendars can lag exchange updates.

## Conflict Handling

- Prefer official exchange, SEBI, registrar, issuer, or BRLM data over aggregators.
- If two official sources conflict, show both values, name the sources, and avoid overconfident conclusions.
- If no source gives a field, write "Not found in checked sources" and list what was checked.
- For volatile data, include "as of" timestamps or access dates.
