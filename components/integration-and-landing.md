# Integration and landing

A result that is verified but not integrated has not landed. This component defines what landing means, and why the shape of integration decides how much autonomy is safe to delegate.

Most projects express this through version control, so the concrete vocabulary below is branches, commits, pull requests, and reverts. The mechanism matters more than the tool: any project with an authoritative state and a way back has the same structure.

## Landing is a separate step from completion

Evidence proves the work. Landing puts it into the state everyone else reads next. These fail independently: a task can be complete and unlanded, and it can be landed while its state document still describes the previous world.

Project state is updated after landing, not after implementation.

## Work on a separate line

Execution happens on a named work line — a branch, a workspace, a copy — never directly on the authoritative one. The authoritative line stays clean, so the question “what is currently true” always has one answer, and landing becomes an explicit transition that a named actor is authorized to make.

## One atomic unit per task

The contract and its implementation land together, as one unit. Separating them lets the record of why drift away from the change itself; landed together, the unit explains its own existence without a second source.

## Revert unit

Delegated landing is licensed by the cost of undoing it. Whatever can be removed in one step is the revert unit, and it is the real measure of how much authority was delegated.

- If one task can be undone alone, an autonomous landing is a bounded mistake.
- If many tasks land as one indivisible unit, undoing one costs all of them, and the remedy becomes larger than the failure it repairs.

So size the unit to the revert you are actually willing to perform. Batching many tasks into a single landing looks efficient and quietly removes the only safety valve the delegation assumed.

## Batches

Group tasks into a batch when review benefits from cross-task patterns, or when landing has fixed overhead. Keep two properties:

- the batch stays small enough that reverting all of it is cheap;
- a batch boundary is a landing, not a stop. Closing one and opening the next is ordinary progress inside a run.

## Landing gate

Before a result becomes authoritative:

1. required evidence exists for every claim in the contract;
2. deterministic checks ran against the exact state being landed — see [Enforcement](evidence-and-verification.md#enforcement) for what a gate can and cannot see at each step;
3. every review finding has a disposition;
4. required human approvals are recorded, not inferred;
5. the state document and the queue are updated to describe the world after this landing.

## Closing invariant

After landing, the workspace should be boring: the authoritative line current, no other open line for the same work, nothing uncommitted, no artifact that exists only in someone’s session. A session that begins by discovering an unclosed landing from the previous one has already lost its orientation.

## Projects without version control

The equivalents are a staging copy, an explicit promotion step, and a recorded way back. If the rollback cannot be described, the promotion should not be delegated.
