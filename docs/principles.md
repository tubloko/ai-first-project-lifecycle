# Principles

These principles describe the current lifecycle. The failure stories in `evolution/` explain how they were earned.

## 1. Use the lowest sufficient level

Complexity has a cost. Add roles, files, reviews, and autonomy only when they address an observed risk.

## 2. The project state must survive the chat

Chats and models can change. Durable decisions, current state, and completion evidence belong in project artifacts.

## 3. Every live fact needs one home

Multiple views may point to a fact, but only one location owns it. Copies become contradictory sources of truth.

## 4. Context should be routed, not accumulated

A new session should receive the smallest complete context for its responsibility. Reading everything is not continuity; it is uncontrolled context growth.

## 5. Roles are defined by responsibility and artifacts

A role requires a mandate, owned knowledge, an output contract, and an authority boundary. A persona description alone does not create reliable specialization.

## 6. Workflow level is not model tier

Levels define process control. Model capability, reasoning effort, and loaded context are routed separately for each responsibility.

## 7. Separate responsibilities when shared context creates bias

Planning, execution, and review can stay together for simple work. Separate them when the planner’s assumptions would weaken implementation or review.

## 8. A task contract carries decisions, not vague intent

Execution should not rediscover product decisions. A ready task names the outcome, scope, constraints, evidence, and stop conditions.

## 9. Authority is not the same as capability

An agent may be technically able to perform an action without being authorized to decide, approve, publish, merge, or change policy.

## 10. Human approval must be explicit

An agent cannot infer a human decision from silence, adjacent evidence, another agent’s summary, or the apparent quality of the result.

## 11. Evidence outranks confident prose

Primary artifacts and deterministic outputs are stronger than an agent’s description of what happened.

## 12. A check must be able to fail

Verification must exercise the claim it reports. A green command that cannot detect the relevant defect is not evidence.

## 13. Reviewer separation is not evidence independence

Multiple review sessions may reduce shared-context bias, but they can still reproduce the same model error. Combine review with deterministic checks, primary artifacts, and human judgment.

## 14. Visual work needs inspectable targets

Words alone are a weak contract for visual output. Use approved references, layout data, captures, comparisons, and explicit human judgment.

## 15. Local correctness does not protect global intent

A sequence of reasonable local changes can move the project away from its intended outcome. Re-anchor work in current laws, decisions, and state—not only the latest implementation.

## 16. Autonomy should grow only as fast as verification

Every increase in autonomous scope needs corresponding evidence, authority boundaries, failure handling, and stop conditions.

## 17. The workflow is also an object of engineering

Record failures, measure recurring costs, test process changes, and retire rules that no longer solve a real problem.
