# Anti-patterns

## Read everything

Loading the full repository into every session increases context without guaranteeing relevance. Route from current state to the smallest complete set of sources.

## Persona without ownership

A named role with no mandate, knowledge base, report format, or authority boundary is role theater.

## Same agent, different hat

Asking one context to plan, implement, then “act as an independent reviewer” does not remove its original assumptions.

## Review count as confidence

Several similar reviewers can reproduce the same error. Count distinct evidence and coverage, not agent messages.

## Parallelism as automatic speed

Concurrent Executors can add dependency discovery, overlapping edits, stale shared state, review-order problems, and integration cost. Parallelize only work with sufficiently independent ownership, inputs, outputs, and landing order.

## Prose as proof

“Tests pass,” “the file exists,” or “the output matches” are claims until the underlying artifacts are inspected.

## Green check that cannot fail

A verifier that does not exercise its claimed boundary creates false confidence.

## Attempts counted as success

Starting a command, generating an empty artifact, or reaching the end of a loop does not prove that every required step succeeded.

## Directory totals as run evidence

Pre-existing artifacts can make a failed run look productive. Report outputs written by the current run separately from stale or reused files.

## Inferred approval

Silence, previous approval, or another agent’s summary cannot satisfy a human-only gate.

## Multiple homes for one fact

Copied rules drift. Keep one editable owner and use links or generated views elsewhere.

## Archive that still routes work

Historical files should not look current. Mark status and prevent normal context routing from treating archives as live instructions.

## Autonomous loop without two stop conditions

A task can fail while a run remains healthy, and a run can become unsafe while an individual task is valid. Define both task-stop and run-stop behavior.

## Review scoped by a range

Comparing two points in history includes everything that entered the workspace between them. Where sessions share a working copy, review then reports other people’s changes as findings against the work in front of it, and every finding is true about the wrong author.

## Stale queue premise

A queue entry describes the project as it was when the entry was written. Work landed since then — including work landed by the current run — may already have satisfied it. Check the premise against current state before implementing it.

## Question as a pause

In most harnesses, asking ends the turn. A question routed to a human mid-run stops the run until a person returns, so a loop that asks is not autonomous, however well it recovers afterwards.

## Unenforced gate

A check that depends on someone remembering to run it is a suggestion. If the binding is not installed with the project, scoped to the change, and provably able to fail, the gate exists only in the documentation.

## Landing without a revert unit

Delegated integration is licensed by the cost of undoing it. If one bad result can only be removed by reverting many unrelated good ones, the safety valve the delegation assumed does not exist.

## Policy changes during the run

An orchestrator should not weaken the gate that blocks its own progress. Record the proposal and route it to the policy owner.

## Pixel similarity as total correctness

A close image can carry the wrong state or action. A different rasterizer can also produce a large diff from a correct implementation. Combine visual and semantic evidence.

## Generated evidence without a recipe

Ephemeral artifacts are acceptable only when a durable, tested entry point can regenerate them from canonical inputs.
