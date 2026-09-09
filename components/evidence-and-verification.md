# Evidence and verification

Completion is a claim. Evidence is what makes the claim inspectable.

## Evidence classes

### Deterministic evidence

Commands, assertions, schema validation, calculations, hashes, and other repeatable checks.

### Primary artifacts

The actual output: changed files, generated assets, captures, diffs, logs, or external records.

### Model review

Reasoned analysis of the output against a contract. Useful for ambiguity and broad coverage, but correlated errors remain possible.

### Human judgment

Required where success is subjective, high-impact, or tied to human authority.

## Claim-to-evidence mapping

Every important acceptance criterion should name:

- the claim;
- the evidence artifact;
- the method used to evaluate it;
- the pass condition;
- known blind spots.

Avoid requirements such as “test the feature” without stating what must be asserted.

## Fail the verifier

Before trusting a new verifier, demonstrate that it detects at least one relevant defect. If practical, run it against a deliberately broken fixture or known failing state.

> A check that cannot fail is decoration.

## Baselines and ratchets

Existing projects often contain known failures. A new gate should prevent regression without blocking every change on unrelated legacy debt.

Record:

- baseline value;
- allowed direction of change;
- scope of the current diff or task;
- conditions that require a full-project gate.

## Enforcement

A gate that runs when someone remembers it is a suggestion. Enforcement is the separate question of how the check becomes unavoidable.

- Bind the gate to the transition it protects — the moment work is recorded, published, or landed — rather than to a habit or a checklist.
- Ship the binding as an installable step. Hook and pipeline wiring that lives outside version control means a fresh clone, a new machine, or a new contributor has no enforcement at all, while the documentation still claims one.
- Scope the gate to the current change. A gate that judges the whole project fails on unrelated legacy debt, and a gate that always fails is bypassed within days. Diff scope is what makes a strict gate survivable, and therefore what makes it real.
- Know what the gate can see at the moment it runs. A check that inspects recorded state measures nothing before the change is recorded: run it after the change is captured and before it is published, or it will report a confident pass over an empty input.
- Make bypass visible rather than impossible. Record who bypassed a gate and why; an untraceable escape hatch is indistinguishable from a gate that passed.
- Prove the gate can fail, on demand. A self-test that deliberately violates the rule is how a baseline earns the authority to block anyone.
- Apply the same enforcement to documentation and process files that carry rules. Prose that governs work drifts exactly like code, and it usually has no test at all.

## Honest accounting

Report what the current run produced, not a directory total containing stale artifacts. Separate:

- artifacts produced now;
- artifacts reused as inputs;
- pre-existing unrelated artifacts;
- skipped or failed steps.

Do not count a task as processed if a required verification step failed or was never executed.

## Review scope

Name the exact output state reviewed. For versioned projects, record a revision identifier. Moving targets create findings that cannot be reproduced.

## Evidence bundle

A Level 3 or Level 4 task should return:

1. outcome summary;
2. exact artifacts changed or produced;
3. verification commands or methods;
4. results with actual values;
5. skipped checks and reasons;
6. review findings;
7. unresolved risk;
8. approval status.

