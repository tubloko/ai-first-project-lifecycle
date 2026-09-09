# Model and context routing

Workflow Level, model capability, reasoning effort, and context size are separate decisions.

A Level describes how work is controlled: which artifacts persist, which responsibilities are separated, what evidence is required, and where authority stops. It does not prescribe one model for the entire project. A Level 4 run may route a routine bounded task to an economical model, while a difficult Level 1 investigation may justify the strongest available reasoning.

## Route by responsibility

Choose a configuration for each responsibility, not for the project as a whole.

| Responsibility | Typical need | Routing preference |
|---|---|---|
| Small deterministic edit | narrow context, explicit change, strong checks | lowest-cost configuration proven reliable for the task |
| State update or triage | accurate reading and disciplined routing | economical configuration with the canonical state only |
| Cross-domain decision | synthesis, ambiguity, trade-offs | higher reasoning capability and broader relevant context |
| Task-contract authoring | resolve decisions and expose missing information | capability sufficient to reason across affected surfaces |
| Bounded execution | follow a settled contract without reopening it | fresh context; capability matched to implementation difficulty |
| Review | inspect one defined risk or evidence surface | configuration suited to the review lens, separated from authorship where useful |
| High-impact approval | accountability and residual-risk acceptance | human authority, supported by evidence rather than replaced by a model |

“Use the strongest model” is not a routing policy. It ignores cost, latency, context pollution, and the fact that a stronger model still cannot repair an undefined contract or an invalid verifier.

## Routing dimensions

Assess at least these dimensions:

- **ambiguity** — how many consequential choices remain unresolved;
- **reasoning depth** — whether the work requires synthesis, planning, or multi-step diagnosis;
- **context breadth** — how many owned sources must be reconciled;
- **impact** — how costly an incorrect result would be;
- **reversibility** — whether the change can be safely undone;
- **verifiability** — whether deterministic or direct evidence can catch mistakes;
- **autonomy** — how far the result may advance without another gate;
- **cost and latency** — what the responsibility is worth spending.

High ambiguity and weak verification usually justify more capable reasoning and a tighter human gate. A narrow task with excellent deterministic checks can often use a cheaper configuration even inside a critical project.

## Context is routed too

Do not compensate for model uncertainty by loading the whole project.

Every responsibility should receive the smallest complete context:

1. its role or task contract;
2. current project state;
3. the canonical sources needed for the decision;
4. relevant prior decisions or reports;
5. explicit exclusions and stop conditions.

Broad-context decision roles may inspect several project surfaces. A fresh Executor should normally receive the resolved task contract and its named references. A Reviewer should receive the claim, output state, and evidence needed for its lens—not the author’s full reasoning transcript.

## Escalation is evidence-driven

Do not silently switch models until an answer looks plausible. When a configuration fails:

1. identify whether the failure came from capability, missing context, an unresolved decision, a broken tool, or invalid verification;
2. repair the contract or evidence path first when that is the actual cause;
3. escalate capability or reasoning effort only when the responsibility genuinely exceeds the current configuration;
4. record the reason when the change affects cost, policy, or repeatability;
5. stop at the authority boundary instead of escalating into an unauthorized decision.

Repeated retries are not independent evidence. A different model may reduce correlated failure, but it does not make review trustworthy without a distinct lens and inspectable artifacts.

## A minimal routing policy

For each recurring responsibility, record:

- default capability tier;
- default reasoning effort;
- required context entry points;
- maximum autonomous authority;
- verification method;
- escalation trigger and destination;
- measured exceptions.

Use [Model routing](../templates/model-routing.md) as a starting point. Keep product names out of the durable policy where possible; map current tools to capability tiers in a replaceable local section.

## What to measure

A routing policy should improve from observed work rather than preference alone. Track:

- first-pass acceptance rate;
- failures by cause;
- human repair time;
- verification escapes;
- cost and latency per accepted result;
- escalation frequency;
- context size only when it helps explain outcomes.

Optimize for reliable accepted results, not the cheapest call or the most impressive individual answer.
