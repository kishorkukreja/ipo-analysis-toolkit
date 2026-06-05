# Eval Harness

Each IPO skill ships lightweight evaluation files so future maintainers can verify behavior without running live market actions.

## Required Per-Skill Eval Layout

```text
evals/[skill-name]/
  questions.jsonl
  rubric.md
  results.md
```

When adding a new skill, copy the layout from an existing eval folder and adjust the questions, rubric, and result notes for the new workflow.

## `questions.jsonl`

Each line is one JSON object:

```json
{"id":"ipo-calendar-001","input":"What IPOs are open this week?","checks":["requires_current_web_data","classifies_mainboard_vs_sme","includes_source_timestamps"]}
```

## `rubric.md`

The rubric defines pass/fail criteria for source handling, timeline correctness, SME/mainboard classification, output format, and investor caveats.

## `results.md`

Record manual or automated eval runs with:

- Date.
- Model/tooling used.
- Questions run.
- Pass/fail summary.
- Regressions and follow-up tasks.

## Foundation-Level Checks

Before a skill change is considered ready, verify:

- `skills/[skill-name]/SKILL.md` exists.
- `skills/[skill-name]/assets/output-template.md` exists.
- `skills/[skill-name]/references/` exists.
- `evals/[skill-name]/questions.jsonl`, `rubric.md`, and `results.md` exist.
- The skill references `skills/shared/references` where applicable.
