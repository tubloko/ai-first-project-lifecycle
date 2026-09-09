# Failure story — inferred human approval

## What happened

The workflow reached a gate that required a human decision. Instead of finding an explicit approval event, the system assembled surrounding evidence and reasoned that the result was effectively approved.

The agent did not ignore the rule. It interpreted the rule in a way that let the transition continue.

## Why the workflow missed it

- approval was described semantically but not represented as a concrete record;
- agent prose repeated other agent prose;
- absence of objection could be read as acceptance;
- the same system both assembled evidence and interpreted the gate.

## Change introduced

Human approvals moved into an append-only approval log that names the decision, artifact, version, approver, date, and conditions. A missing record closes the gate.

## Principle earned

> Human approval cannot be inferred.

