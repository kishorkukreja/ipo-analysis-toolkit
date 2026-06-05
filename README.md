# Indian IPO Skills

Separate installable skills plugin for Indian IPO research workflows across NSE/BSE mainboard and SME issues.

This plugin is intentionally separate from `finance-trading-skills`. Users can install normal trading skills without IPO workflows, or install this IPO plugin independently when they want IPO calendar, DRHP, financials, GMP, subscription, allotment, application, listing-day, and scenario analysis.

## Scope

- Indian IPOs only: NSE/BSE mainboard, NSE Emerge, and BSE SME.
- Retail-investor workflow support, with HNI/SME distinctions where required.
- Research and decision support only. The skills must avoid unsupported investment advice and must state source caveats.

## Skills To Build

The foundation does not create individual skill folders. Each skill thread owns exactly one folder:

| Skill | Purpose |
|---|---|
| `ipo-calendar` | Open, upcoming, and recently listed IPO discovery. |
| `ipo-drhp-analyzer` | DRHP/RHP summary and issue-structure analysis. |
| `ipo-financials-scorer` | Financial quality scorecard from offer documents. |
| `ipo-red-flags-detector` | Warning-sign scan for retail investors. |
| `ipo-peer-comparison` | Listed peer valuation and operating benchmark. |
| `ipo-gmp-tracker` | Grey market premium trend and caveat handling. |
| `ipo-subscription-tracker` | Category-wise subscription and allotment-odds interpretation. |
| `ipo-apply-advisor` | Aggregated apply/avoid/neutral decision support. |
| `ipo-allotment-checker` | Registrar/allotment status workflow. |
| `ipo-listing-day-strategy` | Listing-day scenario and execution planning. |
| `ipo-scenario-simulator` | Bull/base/bear post-listing scenario model. |
| `ipo-application-guide` | Practical IPO application process guide. |

## Current Shared Assumptions

- Default Indian IPO listing timeline is T+3. Do not present T+6 as current default.
- SME IPO process changes apply for issues opening on or after 2025-07-01. Where relevant, distinguish older SME issues from revised process guidance.
- GMP is informal and unregulated. Treat it as sentiment, not as a standalone apply recommendation.
- Mainboard and SME IPOs require different risk, liquidity, lot-size, and process framing.
- Live IPO facts must be sourced from official exchange/SEBI/registrar pages first where practical, then reputable secondary sources with caveats.

## Per-Skill Required Shape

Each skill thread must create:

```text
skills/[skill-name]/SKILL.md
skills/[skill-name]/references/*.md
skills/[skill-name]/assets/output-template.md
evals/[skill-name]/questions.jsonl
evals/[skill-name]/rubric.md
evals/[skill-name]/results.md
```

The shared references are in `skills/shared/references/`. Build instructions and eval rules are in `docs/coordination/`.

## Evaluation Gate

Every skill must pass at least 18 of 20 rubric questions and have no critical failure in source reliability, safety, or regulatory timeline handling before integration.

