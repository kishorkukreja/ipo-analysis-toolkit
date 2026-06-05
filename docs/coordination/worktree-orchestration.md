# Worktree Orchestration

Foundation branch creates this shared plugin skeleton. Skill branches should start from the foundation commit.

Recommended branch naming:

```text
feat/ipo-calendar
feat/ipo-drhp-analyzer
feat/ipo-financials-scorer
feat/ipo-red-flags-detector
feat/ipo-peer-comparison
feat/ipo-gmp-tracker
feat/ipo-subscription-tracker
feat/ipo-apply-advisor
feat/ipo-allotment-checker
feat/ipo-listing-day-strategy
feat/ipo-scenario-simulator
feat/ipo-application-guide
```

Recommended worktree path:

```text
.worktrees/[skill-name]
```

Skill threads must not edit sibling skill folders. Shared files should not be edited from skill branches unless the coordinator explicitly asks for a shared correction.

