# Choosing a level

The four levels are independent operating configurations, not a course and not maturity badges. Choose a level for the work in front of you. Use a higher level only when its added controls solve a real problem.

Independent does not mean interchangeable at any moment. Level 4 automates the Level 3 loop, so it takes a working Level 3 loop as an input: automating a loop that is unreliable by hand produces unreliable results faster, and hides them behind a run report. The choice of level is free; that one prerequisite is not.

Level selection does not select a model. Choose model capability, reasoning effort, and context separately for each responsibility using [Model and context routing](../components/model-and-context-routing.md).

## Quick selector

Start at Level 1 and move down this list only when the answer is yes.

1. Must the work survive a new session, a long pause, or a model change? Use at least Level 2.
2. Would the same context create planning or review bias? Use at least Level 3.
3. Will the workflow repeat tasks without a human driving every transition? Use Level 4.

## Decision dimensions

### Session horizon

- One session: Level 1 may be enough.
- Multiple sessions: Level 2 or higher.
- Multiple tasks and repeated resumptions: Level 3 or 4.

### Decision complexity

- The outcome and method are obvious: Level 1.
- The outcome is stable but context must persist: Level 2.
- The work needs explicit design decisions or specialized review: Level 3.
- The work crosses domains and requires routing or arbitration: Level 4.

### Cost of error

- Cheap and reversible: Level 1.
- Rework would be inconvenient: Level 2.
- Errors could spread into later decisions: Level 3.
- Errors could compound across an autonomous run: Level 4.

### Verification difficulty

- A person can inspect the result directly: Level 1.
- The result needs a durable checklist: Level 2.
- The result needs deterministic evidence and a separate reviewer: Level 3.
- Evidence must gate repeated autonomous transitions: Level 4.

### Autonomy

- Human drives every step: Level 1 or 2.
- Human delegates a bounded task: Level 3.
- Orchestrator selects and advances multiple bounded tasks: Level 4.

## Comparison

| Concern | Level 1 | Level 2 | Level 3 | Level 4 |
|---|---|---|---|---|
| Session count | one | many | many | many |
| Persistent state | task brief | current state + queue | canonical project state | canonical state + run state |
| Planning | same session | same session | separate decision context | orchestrated decision layer |
| Execution | same session | same session | fresh Executor | fresh bounded Executors |
| Review | human inspection | durable checklist | separate review context | multiple selected lenses |
| Domain roles | none | optional reference | report-producing roles | routed specialists |
| Human gates | completion | key decisions | explicit approvals | policy-defined boundaries |
| Autonomous repetition | no | no | no | yes, bounded |

## Upgrade signals

Move up when you repeatedly observe one of these:

- new sessions reconstruct context by guesswork;
- the same question is answered differently across files;
- the planner defends its own assumptions during review;
- work is declared complete without inspectable proof;
- a person spends most of the time copying outputs between agents;
- domain questions are routed to whoever happens to be present;
- an automated loop does not have a clear stop condition.

## Downgrade signals

Move down when:

- coordination costs more than the task;
- reviewers repeat deterministic checks without finding distinct issues;
- persistent artifacts are never reused;
- a single bounded session can safely complete and verify the work;
- the additional roles do not have distinct knowledge or authority.

Using Level 1 inside a Level 4 project is not regression. It is correct sizing.
