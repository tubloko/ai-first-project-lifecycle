# Memory and context

Files can preserve project memory, but an expanding folder is not automatically a usable memory system. This component defines how durable state remains discoverable and current.

## The four memory questions

Every durable artifact should answer:

1. What kind of truth does this file own?
2. Who or which role may update it?
3. When should a session read it?
4. When does it become stale, archived, or replaced?

## Recommended information classes

### Always-current state

The smallest entry point required to resume work: current objective, current position, blockers, and next eligible action.

### Canonical reference

Durable rules, decisions, specifications, and knowledge with a named owner.

### Task artifact

A bounded contract, report, evidence bundle, or review tied to a specific piece of work.

### Generated view

A derived index, summary, render, or report that can be regenerated from canonical sources. It must not silently become a competing source of truth.

### Archive

Historical material retained for provenance or learning. Archived content may explain the past but does not control current work.

## One home per fact

Links and generated views may expose a fact in several places. Editing authority must remain in one canonical home. When a fact moves, update references or provide an explicit compatibility pointer; do not leave two editable copies.

## Context routing

A session should load context in this order:

1. project instructions;
2. current state;
3. the current task contract;
4. only the canonical references named by that task;
5. relevant reports and evidence.

Do not use “read the whole repository” as a default continuity strategy.

## Injected entry point

“Read the current state first” is a request, and a request is honored unevenly across sessions, models, and roles. Where the tool allows it, the entry point should be assembled and placed into the session automatically at start, so the routing order above describes what already happened instead of what a session is expected to remember to do.

An injected entry point is only trustworthy when:

- it is machine-assembled from the canonical sources, so it cannot be edited into disagreement with them;
- the sources delimit the injected regions with explicit markers, so the assembler extracts a named slice instead of guessing at prose;
- it reports the real state of the workspace, including the parts that contradict the state document — an unclosed landing or an unexpected work line belongs in the first thing a session reads;
- it fails loudly. A silent assembler that emits nothing produces a session that believes it is oriented and is not, and that failure is invisible for the rest of the session;
- it stays small. Everything injected is paid for at every session start, so the entry point carries position, queue, blockers, and authority, and names rather than includes the rest.

Pair it with an explicit stop-list: the files a session must not open unless the current task names them. Routing to the smallest complete context is only enforceable when “large, plausible, and out of scope” is written down somewhere.

## Freshness

Time alone does not determine whether information is current. Prefer explicit status:

- `LIVE` — currently authoritative;
- `GENERATED` — derived from named inputs;
- `FROZEN` — intentionally not advancing;
- `RETIRED` — superseded and not valid for new decisions;
- `ARCHIVE` — retained only as historical evidence.

## State-read marker

When reports depend on a moving project, record the exact state examined: date, branch or workspace, and revision identifier when available. A review without a defined state can be correct about the wrong artifact.

