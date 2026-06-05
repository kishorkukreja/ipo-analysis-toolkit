# Registrar Lookup Reference

## Source Order

1. RHP/prospectus, SEBI offer document page, NSE/BSE issue page, or issue notice naming the registrar.
2. Registrar official public issue/allotment page.
3. BSE application status page.
4. NSE Verify IPO Bid/Allotment Details page.
5. Broker or bank app as supporting evidence only.

The registrar is usually the first authoritative public status source after allotment finalisation. Broker, bank, UPI, BSE, and NSE records can lag or reflect only one part of the application flow.

## Major Registrar Status Pages

| Registrar | Official status URL | Common lookup inputs | Notes |
|---|---|---|---|
| KFin Technologies | https://ipostatus.kfintech.com/ | IPO selection plus PAN, application number, or demat account | Do not send users to third-party mirrors. |
| MUFG Intime India, formerly Link Intime | https://in.mpms.mufg.com/Initial_Offer/public-issues.html | PAN, application number, DP/client ID, or account/IFSC when offered | Page may also host Basis of Allotment links and helpdesk details. |
| Bigshare Services | https://ipo.bigshareonline.com/ | Company, application/CAF number, beneficiary ID, PAN, NSDL/CDSL DP details, CAPTCHA | Output may show application number, applied shares, and allotted shares. |
| Maashitla Securities | https://maashitla.com/allotment-status/public-issues | Company, PAN, application number, or demat account number | Common for some SME issues. |
| Purva Sharegistry | https://purvashare.com/investor-service/ipo-query | Company plus application number or PAN | Smaller registrar; verify from prospectus first. |
| Skyline Financial Services | https://www.skylinerta.com/display_ipo_rightissue_allotment.php | Company, DPID/client ID/folio, CAF number, or PAN | Handles IPO and rights issue application status. |
| Cameo Corporate Services | https://ipo.cameoindia.com/ | Company plus PAN, application number, or DP/client ID when offered | Portal behavior can be issue-specific. |
| MAS Services | https://masserv.com/ipoopt.asp | DPID/client ID or PAN | Smaller registrar; exact page may vary. |

For other registrars, verify the registrar name in the RHP/exchange filing and search for the registrar's official public issue status page rather than using aggregator links.

## Exchange Fallbacks

- BSE application status: https://www.bseindia.com/investors/appli_check.aspx
- NSE verify IPO bid/allotment details: https://www.nseindia.com/invest/check-trades-bids-verify-ipo-bids

Use BSE/NSE as cross-checks when the registrar is down, unknown, overloaded, inactive, or the IPO name has not appeared in the registrar dropdown. A "record not found" result on one exchange is not final by itself; ask which exchange/broker route was used and check the registrar/broker record.

## Identifier Minimization

Tell users they may need one of these on the official page:

- PAN.
- Application number.
- DP ID/client ID, beneficiary ID, or demat account number.

Do not ask users to paste these values into chat. If the user already pasted them, do not repeat them back.
