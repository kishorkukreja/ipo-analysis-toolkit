# Troubleshooting And Safety Reference

## Status Interpretation

| Symptom | Likely explanation | Response |
|---|---|---|
| Registrar status not available | Basis not finalized, site not updated, traffic/CAPTCHA issue | Check T+day; retry later; use BSE/NSE fallback. |
| IPO missing from registrar dropdown | Wrong registrar, inactive page, old issue removed, status not published | Verify registrar from RHP/exchange page and use exact issue link. |
| Record not found | Wrong identifier, wrong exchange route, sync lag, rejected bid, bid never submitted | Check broker bid status, application number format, PAN, DP/client ID, and route. |
| PAN works but application number does not | Broker-specific application number format | Try PAN or DP/client ID on the official registrar site. |
| Mandate approved but no record | Bid may not have reached exchange, third-party mismatch, registrar not updated | Verify broker/exchange bid and bank lien; recheck registrar after finalization. |
| Rejected or technical rejection | PAN mismatch, invalid DP/client ID, inactive demat, duplicate application, third-party UPI/bank mismatch, category/lot invalid | Explain likely rejection causes and ask user to confirm broker/registrar reason. |
| Amount debited but shares not visible | Demat credit pending, partial allotment, broker display lag | Check registrar allotted shares and CDSL/NSDL alerts; wait until T+2 evening if still within window. |
| Amount blocked after non-allotment | Bank or sponsor-bank unblock delay | Check lien/hold; contact bank/broker, then registrar; escalate if unresolved. |
| Different registrar/BSE/NSE outputs | Sync lag or route mismatch | Prefer registrar after finalization; cross-check after a few hours. |

## Why No Allotment?

Separate valid non-allotment from rejection:

- In oversubscribed retail/mainboard categories, valid applicants may receive no allotment because minimum-lot allocation is lottery/draw based.
- Applying for more retail lots usually does not guarantee more shares in heavily oversubscribed issues.
- NII/HNI, shareholder, employee, policyholder, and SME individual categories have separate rules; do not map retail logic to every category.
- Technical rejection is different from lottery non-allotment and needs a broker/registrar reason.

## Escalation Flow

1. Check the issue closing date and current T+day.
2. Check registrar status and broker IPO application page.
3. For unblock/refund delay, contact broker and bank with IPO name, application number, date/time, and non-sensitive screenshots.
4. Contact the registrar public issue helpdesk if broker/bank cannot resolve.
5. Use SEBI SCORES only for genuine unresolved grievances after normal processing and intermediary response: https://scores.sebi.gov.in/

## Privacy And Phishing Rules

- Do not ask the user to paste PAN, DP ID/client ID, bank account, IFSC, UPI ID, screenshots, or allotment outputs into chat.
- Tell users to enter identifiers only on the official registrar/exchange HTTPS page.
- Verify the registrar from RHP/prospectus, SEBI, NSE/BSE, or official issue documents before trusting a link.
- Warn against unofficial status-check sites that collect PAN or application details.
- Warn that calls/messages claiming guaranteed allotment, paid allotment help, faster refunds, or mandate release are suspicious.
- Never store or generate URLs containing user identifiers.

## Sources To Prefer

- SEBI T+3 circular: https://www.sebi.gov.in/legal/circulars/aug-2023/reduction-of-timeline-for-listing-of-shares-in-public-issue-from-existing-t-6-days-to-t-3-days_75122.html
- SEBI master circular for issue and listing, including Annexure XXIII: https://www.sebi.gov.in/sebi_data/attachdocs/feb-2026/1770636136785.pdf
- SEBI UPI public issue limit circular: https://www.sebi.gov.in/legal/circulars/apr-2022/revision-of-upi-limits-in-public-issue-of-equity-shares-and-convertibles_57589.html
- SEBI RTAs explainer: https://investor.sebi.gov.in/registrar_and_transfer_agents.html
- SEBI investor safety pages: https://investor.sebi.gov.in/
