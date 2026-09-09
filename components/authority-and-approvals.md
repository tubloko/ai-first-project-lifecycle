# Authority and approvals

Capability answers “can this agent perform the action?” Authority answers “may this role make the decision?” Keep them separate.

## Authority verbs

Define role permissions using explicit verbs:

- **observe** — read and inspect;
- **recommend** — propose a decision;
- **decide** — choose within a declared boundary;
- **change** — modify the project state;
- **approve** — authorize a gated transition;
- **publish** — make an output externally visible;
- **change policy** — alter the rules that govern later work.

Do not infer one verb from another. A role allowed to change a file is not automatically allowed to approve its own change.

## Human-only boundaries

Human ownership is appropriate when the decision requires accountability, identity, high-impact judgment, sensitive context, or acceptance of residual risk.

Examples include:

- changing the project’s intended outcome;
- approving a subjective final composition;
- authorizing irreversible external actions;
- accepting a known high-impact risk;
- expanding an autonomous run’s authority;
- changing the policy that defines approval itself.

## Explicit approval record

A valid approval should identify:

- who approved;
- what exact artifact or decision was approved;
- the state or version reviewed;
- date;
- any conditions or exclusions.

Silence, lack of objection, a neighboring approval, or an agent’s summary is not approval.

## Council decisions

Several domain roles may inform a cross-domain decision. Their agreement is still a set of recommendations unless the authority map grants a named decision role.

Use this pattern:

`Question → separately produced role reports → synthesis → named decision authority → recorded decision`

Do not count multiple restatements of one source as independent confirmation.

## Locked decisions

Some decisions are closed to re-litigation: a value, a boundary, or a definition that later work may use but not reopen. A lock is what keeps a decision durable across sessions that never saw the reasoning behind it, and it is the only defense against a project that re-decides the same question every week with slightly worse information.

A lock may be replaced only by another lock. It is never dissolved by “this no longer seems necessary,” by a session that finds it inconvenient, or by nobody objecting. Unlocking requires all of:

- a new value or rule with named provenance;
- the invariant it holds in place of the one the old lock held — and if nothing is being protected any more, say so explicitly, because retiring a constraint is a larger decision than replacing one;
- a record in every canonical home the old lock occupied, so the old value cannot survive somewhere as a live copy;
- two independent signatures, where the second is not a rubber stamp: it comes from a role given only the proposal and its evidence, not the conversation that produced them.

Granting an autonomous workflow the authority to unlock without this procedure is not delegation. It is permission to undo earlier decisions one at a time, and it looks like progress while it is happening.

## Fail-closed transitions

When a required approval is missing or ambiguous:

1. keep the gate closed;
2. preserve the work as a draft;
3. state exactly what decision is missing;
4. continue only with unrelated work that remains authorized.
