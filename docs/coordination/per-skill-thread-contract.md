# Per-Skill Thread Contract

Each skill thread owns exactly one skill and one branch/worktree.

Goal format:

```text
Create, evaluate, and improve [skill-name] until its 20-question rubric eval reaches 90%+ pass rate.
```

## Required Reads

- `finance-trading-skills/docs/ipo-skills-design-decisions.md`
- `finance-trading-skills/docs/ipo-skills-plan.md`
- `finance-trading-skills/docs/research/ipo/[skill-name]/research.md`
- Shared references in this plugin when relevant.

## Required Writes

```text
skills/[skill-name]/SKILL.md
skills/[skill-name]/references/*.md
skills/[skill-name]/assets/output-template.md
evals/[skill-name]/questions.jsonl
evals/[skill-name]/rubric.md
evals/[skill-name]/results.md
```

## Eval Dataset Coverage

Create exactly 20 JSONL questions covering:

- Happy path.
- Missing-data behavior.
- SME vs mainboard distinctions.
- Current T+3 timeline rules.
- July 2025 SME process handling where relevant.
- Source hierarchy and caveats.
- Output template compliance.
- Safety boundary against unsupported investment advice.

## Pass Gate

The skill is complete only when:

- At least 18 of 20 questions pass.
- No critical source-reliability failure remains.
- No critical safety failure remains.
- No critical regulatory-timeline failure remains.
- The final `results.md` lists score, failed cases if any, files created, and remaining risks.

