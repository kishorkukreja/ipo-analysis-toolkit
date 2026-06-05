# Skill Build Matrix

Use this matrix to assign and verify the 12 skill branches. This document names target paths only; the foundation intentionally does not create these folders.

| Skill | Target skill path | Target eval path | Research source |
|---|---|---|---|
| `ipo-calendar` | `skills/ipo-calendar/` | `evals/ipo-calendar/` | `../finance-trading-skills/docs/research/ipo/ipo-calendar/research.md` |
| `ipo-drhp-analyzer` | `skills/ipo-drhp-analyzer/` | `evals/ipo-drhp-analyzer/` | `../finance-trading-skills/docs/research/ipo/ipo-drhp-analyzer/research.md` |
| `ipo-financials-scorer` | `skills/ipo-financials-scorer/` | `evals/ipo-financials-scorer/` | `../finance-trading-skills/docs/research/ipo/ipo-financials-scorer/research.md` |
| `ipo-red-flags-detector` | `skills/ipo-red-flags-detector/` | `evals/ipo-red-flags-detector/` | `../finance-trading-skills/docs/research/ipo/ipo-red-flags-detector/research.md` |
| `ipo-peer-comparison` | `skills/ipo-peer-comparison/` | `evals/ipo-peer-comparison/` | `../finance-trading-skills/docs/research/ipo/ipo-peer-comparison/research.md` |
| `ipo-gmp-tracker` | `skills/ipo-gmp-tracker/` | `evals/ipo-gmp-tracker/` | `../finance-trading-skills/docs/research/ipo/ipo-gmp-tracker/research.md` |
| `ipo-subscription-tracker` | `skills/ipo-subscription-tracker/` | `evals/ipo-subscription-tracker/` | `../finance-trading-skills/docs/research/ipo/ipo-subscription-tracker/research.md` |
| `ipo-apply-advisor` | `skills/ipo-apply-advisor/` | `evals/ipo-apply-advisor/` | `../finance-trading-skills/docs/research/ipo/ipo-apply-advisor/research.md` |
| `ipo-allotment-checker` | `skills/ipo-allotment-checker/` | `evals/ipo-allotment-checker/` | `../finance-trading-skills/docs/research/ipo/ipo-allotment-checker/research.md` |
| `ipo-listing-day-strategy` | `skills/ipo-listing-day-strategy/` | `evals/ipo-listing-day-strategy/` | `../finance-trading-skills/docs/research/ipo/ipo-listing-day-strategy/research.md` |
| `ipo-scenario-simulator` | `skills/ipo-scenario-simulator/` | `evals/ipo-scenario-simulator/` | `../finance-trading-skills/docs/research/ipo/ipo-scenario-simulator/research.md` |
| `ipo-application-guide` | `skills/ipo-application-guide/` | `evals/ipo-application-guide/` | `../finance-trading-skills/docs/research/ipo/ipo-application-guide/research.md` |

## Shared References

All skill threads may read:

- `skills/shared/references/india_ipo_data_sources.md`
- `skills/shared/references/sme_vs_mainboard.md`
- `skills/shared/references/registrars.md`
- `docs/conventions/shared-ipo-conventions.md`
- `CLAUDE.md`

## Foundation Acceptance Criteria

- No individual IPO skill folder exists before per-skill work starts.
- `skills/shared/references` exists and contains common guidance.
- `evals/_template` exists and defines the required eval shape.
- `.gitignore` ignores `.worktrees/` and `worktrees/`.
- Git repo is initialized and has an initial foundation commit.
