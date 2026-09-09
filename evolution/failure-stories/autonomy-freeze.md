# Failure story — autonomy grew faster than trust

## What happened

The Autopilot could produce tasks, route them, review results, and advance the queue. Its speed exposed a deeper issue: the system could complete process steps faster than it could establish whether their evidence and authority were valid.

Several individually plausible signals combined into false confidence:

- multiple summaries repeated one underlying source;
- reviewers examined moving or insufficiently identified state;
- a council answered questions outside its authority;
- gates trusted prose about checks rather than the checks themselves;
- the orchestrator had incentives to continue the run.

## Response

Autonomous operation was frozen. The project audited source provenance, ownership, approval semantics, verifier behavior, and review scope before allowing the loop to resume.

## Change introduced

- bounded run budgets;
- separate task and run stop conditions;
- explicit authority maps;
- revision-scoped evidence and review;
- per-task review before advancement;
- an abort path that does not count as task completion;
- human-only boundaries the Autopilot cannot redefine.

## Principle earned

> Autonomy should grow only as fast as verification.

