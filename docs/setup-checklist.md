# Setup checklist

Use this checklist after adopting or changing a Level.

## Scope

- [ ] The selected Level is named.
- [ ] The concrete workstream using it is named.
- [ ] A lower Level was considered.
- [ ] Optional pipelines are included only for outputs that need them.

## Memory

- [ ] The project has one current-state entry point when continuity is required.
- [ ] Every live fact has one canonical home.
- [ ] Archives are visibly non-authoritative.
- [ ] Generated views name their inputs.
- [ ] New sessions are not instructed to read everything.
- [ ] The current-state entry point is injected or read before work begins, and its assembler fails loudly when it produces nothing.

## Roles

- [ ] Every persistent role has a mandate.
- [ ] Every role has an output contract.
- [ ] Reusable knowledge and project reports are separate.
- [ ] Each role’s authority boundary is explicit.
- [ ] No two roles own the same fact.

## Model and context routing

- [ ] Model capability is selected per responsibility, not per project or Level.
- [ ] Every recurring responsibility has a minimal complete context entry point.
- [ ] Escalation distinguishes capability failure from missing context, unresolved decisions, and broken verification.
- [ ] A stronger model does not bypass an authority gate.
- [ ] Repeated retries are not counted as independent evidence.

## Tasks

- [ ] The next task has an observable outcome.
- [ ] Required decisions are resolved before execution.
- [ ] In-scope and out-of-scope boundaries are explicit.
- [ ] Stop conditions prevent guessing.
- [ ] Completion evidence is named before work begins.
- [ ] The contract names the exact verification command and its expected values.
- [ ] Expectations the task invalidates are listed by file and line.

## Review and evidence

- [ ] The result can be inspected independently of the agent’s summary.
- [ ] Deterministic checks exercise the claim they report.
- [ ] A new verifier has demonstrated a relevant failure.
- [ ] Review scope names an exact artifact state.
- [ ] Blocking findings cannot disappear without disposition.
- [ ] Each gate is bound to the transition it protects, installed with the project, scoped to the change, and shown to fail on a deliberate violation.

## Authority

- [ ] Human-only decisions are listed.
- [ ] Approval requires an explicit record.
- [ ] A role cannot approve its own work unless that authority is deliberately granted.
- [ ] Policy changes have a named owner.
- [ ] High-impact or irreversible actions have appropriate controls.

## Autonomy

- [ ] The manual Level 3 loop works before Level 4 is enabled.
- [ ] The run has an objective and budget.
- [ ] Task-stop and run-stop conditions are distinct.
- [ ] Repair attempts are bounded.
- [ ] The orchestrator cannot widen its own authority.
- [ ] Queue entries are checked against current state before a contract is written.
- [ ] An authority gap aborts the task instead of stopping the run.
- [ ] Landed work has a named revert unit, small enough to undo alone.
- [ ] The run always produces a final report.

## Result

If any required item is unresolved, either repair the setup or use a lower Level until the missing boundary can be defined.
