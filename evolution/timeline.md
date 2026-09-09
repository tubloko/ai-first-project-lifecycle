# Evolution

This lifecycle did not begin as a complete architecture. A deliberately ambitious side project started with files, a chat, and a simple implementation sequence. Each later layer answered a failure exposed by the previous one.

## 0. Project file, phases, and tasks

The project began with a durable MVP document. That document was divided into large phases and a task list.

`Project file → phases → task list → implementation`

The project never lived only in chat. Files were present from the beginning.

## 1. More sessions, more files

Work continued through new chats and accumulated documents. Continuity existed, but finding the current truth became harder as status, context, journals, plans, and task notes grew.

The problem was file entropy, not absence of files.

## 2. Routed continuity

Start and end protocols appeared. A small current-state pointer directed each new session to the relevant context instead of asking it to read everything.

Over time, redundant files were retired and canonical homes became explicit.

## 3. Brain and Executor

Planning and implementation were separated. A broad-context Brain wrote a detailed contract; a fresh Executor received only the context required to perform it.

This reduced context growth and allowed model effort to be chosen by responsibility.

## 4. Independent review contexts

The Brain initially reviewed work shaped by its own assumptions. Separate reviewers were added so the author of a contract was no longer its only evaluator.

Review first happened at the end of a batch and later moved closer to each task.

## 5. Domain roles learn through research

Recurring knowledge gaps produced specialized roles. Each role researched authoritative sources, built an owned knowledge base, and wrote dated project reports.

`Knowledge gap → role mandate → sourced research → knowledge base → project report`

This replaced persona-only specialization with durable knowledge and artifact contracts.

## 6. Human as middleware

As the number of roles and tasks grew, the human spent increasing time transporting specs, reports, and questions between sessions.

An Architect role helped examine process gaps, and an Autopilot began orchestrating the existing lifecycle.

## 7. Domain routing

The Autopilot still escalated questions that the human was not best placed to answer. Routing changed: domain questions went to the relevant roles, cross-domain reports went to a named decision authority, and only human-owned boundaries returned to the human.

## 8. Visual asset production becomes a pipeline

Generated images moved from ad hoc outputs into a controlled sequence of briefs, references, candidates, approval, normalization, and an asset index.

The artifact and its provenance became more important than the generation chat.

## 9. Mocks become implementation targets

Visual implementation needed a more precise target than prose. Approved mocks produced deterministic renders and layout data. Runtime captures could then be compared against the intended output.

## 10. The visual verifier tests the wrong thing

Raw pixel comparison treated rendering-engine differences as implementation defects. Fonts, viewport assumptions, and impossible thresholds produced confident but misleading results.

Visual verification expanded to combine pixels, regions, geometry, semantics, and human judgment.

## 11. Direct design-tool experiments stay experiments

Several ways of working directly inside visual design environments were tested. In this project, agents were more reliable when the target could be represented as inspectable files, deterministic renders, layout data, and explicit comparison artifacts.

The experiments remained part of the history rather than becoming a mandatory dependency. A tool that fits one stage does not need to become the foundation of the lifecycle.

## 12. Local correctness creates global drift

Each task could be reasonable relative to the previous implementation while the overall project moved away from its intended reality.

The workflow was re-anchored:

`Intended rules and states → approved mocks and contracts → implementation`

instead of:

`Current implementation → next local improvement → next local improvement`

## 13. Documentation becomes a versioned system

Documentation had existed from the start, but it also accumulated transitional artifacts and lived across changing locations. Cleaning it exposed a second-order problem: project memory needs its own versioning, ownership, archive rules, and reproducible history.

Live, generated, archived, and retired information became distinct states. Moving a fact no longer meant leaving an active-looking copy behind.

## 14. Laws, ownership, and gates

Important constraints gained canonical homes, domain owners, explicit authority, and transition gates. Human-only approval became a recorded event rather than an inference.

## 15. Autonomy outruns evidence

The Autopilot could advance work faster than the evidence system could justify it. Agent summaries were mistaken for primary proof, repeated claims looked like independent confirmations, and some checks could not detect the defects they claimed to cover.

Autonomous operation was frozen while the process was audited.

## 16. Trust rebuild

The rebuild added or strengthened:

- provenance ranking;
- one canonical home per fact;
- explicit approval records;
- review against an exact project revision;
- fail-closed gates;
- executable verification;
- honest success accounting;
- task-level and run-level stop conditions.

## 17. Bounded autonomy returns

Autopilot returned with bounded batches, per-task evidence, selected review lenses, escalation rules, and explicit human-only decisions.

## 18. Parallel execution exposes coordination cost

Running several Executors at once looked like an obvious speedup. In practice, dependency discovery, overlapping changes, shared state, review order, and integration conflicts could erase the gain.

Parallelism became a routing decision rather than a default. Work should run concurrently only when its ownership, inputs, outputs, and landing order are sufficiently independent.

## 19. The workflow becomes measurable

The project began testing its own assumptions: model assignment, reviewer context, prompt shape, task size, verification coverage, and coordination cost.

The lifecycle remains changeable, but changes are now treated as hypotheses rather than automatic improvements.
