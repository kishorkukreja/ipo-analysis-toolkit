# Indian IPO Skills

Standalone skills plugin for Indian IPO research workflows across NSE/BSE mainboard, NSE Emerge, and BSE SME issues.

Use this toolkit when you need IPO calendar, DRHP, financials, GMP, subscription, application, allotment, listing-day, and scenario analysis for Indian public issues.

## Install

Clone the repository:

```powershell
git clone https://github.com/kishorkukreja/ipo-analysis-toolkit.git
cd ipo-analysis-toolkit
```

Install it as a local skills/plugin bundle in your agent or Codex setup. Keep the repository layout intact because several skills use shared references from `skills/shared/references`.

The runtime files are:

```text
skills/
docs/
AGENTS.md
CLAUDE.md
```

Recommended local install pattern:

```powershell
$repo = "C:\path\to\ipo-analysis-toolkit"
$plugins = "$HOME\.codex\plugins"
New-Item -ItemType Directory -Force $plugins
New-Item -ItemType Junction -Path "$plugins\ipo-analysis-toolkit" -Target $repo
```

If your agent supports a configured skills/plugin path, point it at the cloned repository root, not at one individual skill folder.

Manual fallback:

```powershell
$repo = "C:\path\to\ipo-analysis-toolkit"
$skillsRoot = "$HOME\.codex\skills"
New-Item -ItemType Directory -Force $skillsRoot
Copy-Item "$repo\skills\*" $skillsRoot -Recurse -Force
```

The fallback is less ideal because the skills were authored as one bundle with shared references. If you use it, keep `skills/shared/references` available alongside the IPO skill folders.

The `evals/` folder is included as quality evidence and regression material. It is not required at runtime, but it is useful when changing a skill.

## Skills

| Skill | Use it when the user asks for... |
|---|---|
| `ipo-calendar` | Open, upcoming, recently closed, or recently listed Indian IPOs. |
| `ipo-drhp-analyzer` | DRHP/RHP/prospectus summaries, issue structure, objects of issue, risk factors, promoter details, litigation, or offer-document extraction. |
| `ipo-financials-scorer` | A financial quality scorecard using revenue, margins, ROE/ROCE, debt, CFO, working capital, and sector adjustments. |
| `ipo-red-flags-detector` | Governance, accounting, promoter, litigation, RPT, auditor, pledge, OFS, SME, or disclosure warning signs. |
| `ipo-peer-comparison` | Valuation against listed peers, DRHP peer-table audits, premium/discount framing, and fair/expensive/cheap interpretation. |
| `ipo-gmp-tracker` | Grey market premium level, trend, source reliability, implied listing price, and GMP caveats. |
| `ipo-subscription-tracker` | Category-wise subscription, QIB/NII/retail demand quality, anchor quality, and rough retail allotment odds. |
| `ipo-apply-advisor` | Final apply/avoid/neutral synthesis after combining financials, red flags, valuation, GMP, and subscription data. |
| `ipo-allotment-checker` | Registrar lookup workflow, allotment status, UPI mandate/refund troubleshooting, and BOA/status caveats. |
| `ipo-listing-day-strategy` | Listing-day sell/hold planning, opening-price scenarios, stop levels, order-type cautions, and tax notes. |
| `ipo-scenario-simulator` | Bull/base/bear post-listing scenarios, valuation rerating, lock-in overhang, and 6- or 12-month ranges. |
| `ipo-application-guide` | How to apply through UPI/ASBA, category selection, cut-off bidding, bid revision/cancellation, and SME process handling. |

## Usage Examples

Ask for a specific skill by name when you want a focused workflow:

```text
Use ipo-calendar to list Indian mainboard and SME IPOs open this week. Include source timestamps and separate SME issues.
```

```text
Use ipo-drhp-analyzer for this DRHP: [paste URL]. Summarize issue structure, objects of issue, top risks, promoter background, litigation, related-party transactions, and retail caveats.
```

```text
Use ipo-financials-scorer on this RHP and give me the 100-point scorecard with revenue growth, margins, ROE/ROCE, debt, CFO/PAT, working-capital quality, and confidence.
```

```text
Use ipo-red-flags-detector for this SME IPO. Focus on related-party transactions, customer concentration, auditor notes, sudden profit spikes, use of proceeds, and liquidity risk.
```

```text
Use ipo-peer-comparison to compare this IPO valuation with listed peers. Audit whether the DRHP peer set is fair and explain the premium or discount.
```

```text
Use ipo-gmp-tracker for this IPO. Compare GMP across sources, calculate implied listing price, assess trend reliability, and tell me what GMP can and cannot prove.
```

```text
Use ipo-subscription-tracker for day 3 data. Interpret QIB, NII, retail, anchor quality, and estimate retail allotment odds with caveats.
```

```text
Use ipo-apply-advisor to combine the DRHP, financial score, red flags, peer valuation, GMP, and subscription data. End with Apply, Neutral, or Avoid and explain listing-gain vs long-term logic.
```

```text
Use ipo-allotment-checker. The IPO closed on 2026-06-03 and I applied through UPI. Tell me where to check allotment, what dates to expect under T+3, and what to do if my mandate is still blocked.
```

```text
Use ipo-listing-day-strategy. I got allotment and want a listing-day plan with sell zones, hold conditions, stop logic, tax caveats, and order-type warnings.
```

```text
Use ipo-scenario-simulator to build 6-month bull/base/bear scenarios after listing. Include peer multiples, lock-in supply overhang, liquidity, and confidence.
```

```text
Use ipo-application-guide. Explain whether I should apply as retail, sHNI, bHNI, or SME individual, how cut-off bidding works, and when cancellation or bid reduction is allowed.
```

You can also let the agent route the request naturally:

```text
Analyze this IPO end to end for a retail investor. Start with DRHP extraction, then financial score, red flags, peers, GMP, subscription, and final apply/avoid/neutral synthesis.
```

## Current Indian IPO Assumptions

- Current default public issue listing timeline is T+3 working days from issue close. Treat T+6 as historical unless an older issue or official document proves otherwise.
- SME IPO process changes apply for issues opening on or after 2025-07-01. Distinguish pre-change and post-change SME issues before giving application-process guidance.
- GMP is informal, unregulated, and not guaranteed. Use it as a sentiment input, never as a standalone apply recommendation.
- Mainboard and SME IPOs require different risk, liquidity, lot-size, process, and exit-friction framing.
- Prefer official sources first: SEBI, NSE, BSE, issuer, BRLM, registrar, and offer documents. Use secondary sources only with caveats.

## Scorecard Model

Department skills can emit 0-100 scores with confidence and evidence quality. `ipo-apply-advisor` aggregates them through a weighted model:

| Department | Weight |
|---|---:|
| Financial quality | 25% |
| Valuation / peer comparison | 20% |
| Governance, red flags, and issue structure | 20% |
| Demand quality: subscription, anchors, category mix | 15% |
| GMP / listing sentiment / market mood | 10% |
| Application fit, liquidity, timeline, and execution risk | 10% |

The weighted score is not mechanical. Hard gates and confidence caps override the raw score, so missing primary documents, secondary-only subscription data, conflicting GMP, serious governance issues, weak cash conversion, or expensive pure-OFS structures can keep the verdict at `Neutral` or `Avoid`.

## Quality Checks

Each skill includes:

```text
skills/[skill-name]/SKILL.md
skills/[skill-name]/references/*.md
skills/[skill-name]/assets/output-template.md
evals/[skill-name]/questions.jsonl
evals/[skill-name]/rubric.md
evals/[skill-name]/results.md
```

All 12 skills were evaluated with 20-question rubric datasets. The integration gate is at least 18/20 pass rate and zero critical failures in source reliability, safety, and regulatory-timeline handling.
