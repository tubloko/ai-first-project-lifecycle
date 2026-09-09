# Review and triage

Review finds problems. Triage decides what happens to them. Keeping those responsibilities separate prevents a Reviewer from silently changing scope or accepting its own risk decisions.

## Reviewer contract

A Reviewer receives:

- the task contract;
- the exact output state or revision;
- relevant primary artifacts;
- verification results;
- a specific review question or lens.

It returns structured findings. By default it does not edit, approve, integrate, or change policy.

## Review lenses

Select lenses because they inspect distinct risks, for example:

- contract compliance;
- correctness;
- user-facing clarity;
- domain validity;
- security or privacy;
- maintainability;
- evidence integrity;
- scope drift.

Do not dispatch several generic reviewers and treat agreement as independent proof.

In a repeating autonomous run, prefer a fixed lens set dispatched concurrently over lenses chosen per task. See [Review lenses](../levels/4-governed-autonomy.md#review-lenses).

## Inbox rule

The review inbox is normally empty. It contains unresolved findings, not a second backlog and not a history archive.

Every finding records:

- exact review scope;
- evidence;
- impact;
- priority;
- recommended disposition;
- authority required.

## Triage dispositions

### Fix

The finding is valid and must be resolved before acceptance.

### Accept risk

The finding is valid, but the named authority explicitly accepts the consequence.

### Defer

The finding is valid but outside the current contract. Move it to the canonical queue with a reference back to the finding.

### Invalid

The finding is unsupported, out of scope, based on stale state, or contradicted by stronger evidence. Record why.

## Completion invariant

A task cannot be accepted while a blocking finding has no disposition. “Reviewer finished” is not the same as “review passed.”

## Review timing

Batch-level review can find cross-task patterns but allows defects to compound. Task-level review reduces that delay. Use both only when each has distinct coverage.

