# Sample workspace

This filled example demonstrates a Level 3 project with a persistent domain role and an explicit approval gate. It is intentionally small enough to inspect without additional tooling.

## Scenario

Project Atlas is preparing a public onboarding guide. The next task is to create the approved structure for the guide’s landing page. The decision depends on a short research report, then moves through a Task Contract, execution evidence, separate review, and human acceptance.

## Map

```text
sample-workspace/
├── PROJECT.md
├── CURRENT_STATE.md
├── tasks/T-001-onboarding-page.md
├── decisions/D-001-page-structure.md
├── approvals/APPROVALS.md
├── evidence/T-001.md
└── roles/research/
    ├── ROLE.md
    ├── knowledge_base/INDEX.md
    └── reports/2026-01-10-onboarding-structure.md
```

## Reading order

1. [PROJECT.md](PROJECT.md)
2. [CURRENT_STATE.md](CURRENT_STATE.md)
3. [Research role](roles/research/ROLE.md)
4. [Research report](roles/research/reports/2026-01-10-onboarding-structure.md)
5. [Decision](decisions/D-001-page-structure.md)
6. [Task Contract](tasks/T-001-onboarding-page.md)
7. [Evidence](evidence/T-001.md)
8. [Approval log](approvals/APPROVALS.md)

These files are filled examples, not alternate templates. The canonical templates remain in [`templates/`](../../templates/).

