# Glossary

## Approval

An explicit decision by the authority responsible for a boundary. Approval cannot be inferred by an agent.

## Architect

A role that resolves technical trade-offs and cross-system impact. It does not automatically own product intent or human-only decisions.

## Authority boundary

The explicit limit between what a role may observe, recommend, decide, change, or approve.

## Autopilot

An orchestrator that advances a bounded run across multiple tasks. It coordinates existing roles and gates; it does not receive unlimited authority.

## Brain

The decision layer that selects the next meaningful task, resolves required decisions, and writes the task contract.

## Canonical home

The single live location that owns a fact or artifact.

## Domain role

A specialized role with a mandate, sourced knowledge base, project-specific reports, and an authority boundary.

## Evidence

An inspectable artifact that supports a completion or decision claim. Evidence may be deterministic, visual, human-authored, or model-generated, but its origin must be clear.

## Execution harness

The exact command that verifies a task, its expected values, and the fixtures those values come from, carried inside the task contract so the Executor does not have to rediscover how the project is run.

## Executor

A role or fresh session responsible for completing a bounded task contract without reopening settled decisions.

## Landing

The transition that makes a completed result part of the authoritative project state. Distinct from completion: work can be finished and unlanded.

## Gate

A transition condition that must be satisfied before work advances. A gate may be deterministic, reviewer-based, or human-only.

## Knowledge base

Reusable domain knowledge owned by a role. It is distinct from reports about a specific project state.

## Project state

The smallest durable representation of where the project is, what is true, and what should happen next.

## Routing policy

The mapping from a responsibility to its default capability, effort, context entry points, verification, escalation, and authority limit.

## Report

A dated analysis or verdict about a specific question and project state. Reports are outputs; they do not silently become universal knowledge.

## Revert unit

The smallest amount of landed work that can be removed in one step. It measures how much authority an autonomous landing actually carries.

## Reviewer

A separate evaluation context that examines evidence and output against a contract. A Reviewer reports findings unless explicitly granted another authority.

## Run

A bounded sequence of one or more tasks with explicit exit conditions.

## Task contract

A self-contained artifact that defines the desired outcome, resolved decisions, boundaries, verification, and completion report.

A Task Spec is the concrete file that carries this contract in Levels 3 and 4. “Contract” describes its function; it does not imply a legal agreement.
