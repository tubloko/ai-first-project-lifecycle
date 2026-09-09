# Sample project

This example shows how one project can use different Levels without maintaining four separate workflows.

## Project state

The project has:

- a durable objective;
- an active work queue;
- several domain decisions;
- visual deliverables;
- a mixture of routine and high-impact tasks.

Shared canonical components live once: current state, decisions, approvals, role knowledge, reports, and evidence.

## Work item A — organize a short list

The outcome is clear, reversible, and inspectable in one session.

Use **Level 1**:

`Task Brief → Work → Human inspection → Result`

Do not invoke persistent roles or create a Task Contract.

## Work item B — research a domain question across sessions

The work must survive a pause and preserve sources.

Use **Level 2** plus the Research pipeline:

`Current State → Research Brief → Sourced Notes → Report → Updated State`

Create a persistent Domain Role only if the knowledge gap will recur.

## Work item C — implement an approved visual interface

The work has settled intent, measurable geometry, and a result that should not be reviewed only by its author.

Use **Level 3** plus the Mock-to-Implementation pipeline:

`Brain → Task Contract → Fresh Executor → Runtime Capture → Pixel/Geometry/Semantic Evidence → Reviewer → Human Visual Gate`

The mock, layout data, and approval record stay in their canonical homes. The Level references them; it does not duplicate them.

## Work item D — process a stable queue

The Level 3 loop has already succeeded repeatedly by hand. Eligible tasks have clear contracts, verification, and stop conditions.

Use **Level 4**:

`Autopilot → Task → Evidence → Review → Landing Gate → State Update → Next Eligible Task`

If a task crosses a human-only boundary, Autopilot parks that task and either continues with unrelated authorized work or ends the run according to policy.

## Result

The project does not “become Level 4.” It uses Level 4 where repeated autonomy is justified and keeps simpler work simple.
