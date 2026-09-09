# Task contract

**ID:**  
**Outcome owner:**  
**Execution owner:**  
**Decision state:** READY | NOT READY

## 0. Readiness

List every unresolved decision. If any required decision remains unresolved, this contract is not ready for execution.

## 1. Outcome

Describe the observable result, not merely the activity.

## 2. State and references

- Project state examined:
- Canonical references:
- Relevant reports:
- Superseded material that must not be used:

## 3. Resolved decisions

- Decision — authority — rationale or record.

## 4. In scope

- 

## 5. Out of scope

- 

## 6. Constraints

- 

## 7. Work units

### Unit 1

- Required result:
- Dependencies:
- Allowed files or surfaces:
- Prohibited changes:

## 8. Evidence and acceptance

| Claim | Evidence | Evaluation method | Pass condition | Blind spots |
|---|---|---|---|---|
|  |  |  |  |  |

### Harness

- Exact command that runs the verification:
- Expected result of that command, as concrete values:
- Where those expected values come from:

An Executor that has to discover how to run the project spends its first and most expensive stretch orienting instead of working. The command belongs in the contract even when it feels obvious to whoever wrote it.

### Expectations this task invalidates

| Fixture, golden, or assertion | File | Line or identifier | Survives this task | Replacement |
|---|---|---|---|---|
|  |  |  |  |  |

A contract that changes a value, a shape, or a version must list every existing expectation that change invalidates, located by file and line. “Do not edit the tests” and “the suite stays green” cannot both hold while an unlisted expectation still encodes the premise this task removes.

Enumerate by the state being made unreachable, not by the name of the mechanism being changed: fixtures that construct that state through some other door break too, and they are the ones a search for the mechanism will miss.

## 9. Stop conditions

Stop and report when:

- a required source is missing or contradictory;
- an unresolved decision would change the result;
- work crosses the authority or scope boundary;
- required evidence cannot be produced;
- the measured state contradicts this contract.

## 10. Report back

1. Outcome summary.
2. Artifacts changed or produced.
3. Verification results with actual values.
4. Skipped checks and reasons.
5. Residual findings or risks.
6. Revision or state identifier.

