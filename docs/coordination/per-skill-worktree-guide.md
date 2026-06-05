# Per-Skill Worktree Guide

This repository is prepared for isolated per-skill branches or worktrees.

## Rules For Skill Threads

- Work only inside `indian-ipo-skills`.
- Do not modify `finance-trading-skills`.
- Do not create files for skills other than the assigned skill.
- Reuse `skills/shared/references` instead of duplicating shared source guidance.
- Copy `evals/_template` into `evals/[skill-name]` and specialize it.

## Required Paths

For assigned skill `[skill-name]`, create:

```text
skills/[skill-name]/SKILL.md
skills/[skill-name]/references/
skills/[skill-name]/assets/output-template.md
evals/[skill-name]/questions.jsonl
evals/[skill-name]/rubric.md
evals/[skill-name]/results.md
```

Example for `ipo-calendar`:

```text
skills/ipo-calendar/SKILL.md
skills/ipo-calendar/references/
skills/ipo-calendar/assets/output-template.md
evals/ipo-calendar/questions.jsonl
evals/ipo-calendar/rubric.md
evals/ipo-calendar/results.md
```

## Research Source

Use the existing research as read-only input:

```text
../finance-trading-skills/docs/research/ipo/[skill-name]/research.md
```

Do not move or rewrite the research source unless a separate task explicitly asks for it.

## Branch Naming

Recommended branch names:

```text
skill/ipo-calendar
skill/ipo-drhp-analyzer
skill/ipo-financials-scorer
skill/ipo-red-flags-detector
skill/ipo-peer-comparison
skill/ipo-gmp-tracker
skill/ipo-subscription-tracker
skill/ipo-apply-advisor
skill/ipo-allotment-checker
skill/ipo-listing-day-strategy
skill/ipo-scenario-simulator
skill/ipo-application-guide
```

## Pre-Handoff Verification

Run non-destructive checks before handing off:

```powershell
git status --short
git check-ignore -q .worktrees; if ($LASTEXITCODE -eq 0) { "worktrees ignored" } else { "worktrees not ignored" }
Test-Path "skills/[skill-name]/SKILL.md"
Test-Path "skills/[skill-name]/assets/output-template.md"
Test-Path "evals/[skill-name]/questions.jsonl"
```
