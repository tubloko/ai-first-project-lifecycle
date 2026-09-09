# Standard task pipeline

This is the reusable unit beneath all four levels. Higher levels separate its responsibilities across more contexts and add stricter gates.

## Flow

`Intent → Contract → Work → Evidence → Review → Acceptance → Memory update`

## Intent

State the observable outcome. Do not begin with a tool or implementation method unless that method is itself a constraint.

## Contract

Capture scope, resolved decisions, references, constraints, verification, stop conditions, and reporting requirements. Choose the Task Brief or Task Spec template according to the selected Level.

## Work

Perform only authorized changes. Surface contradictions rather than resolving them by silently expanding scope.

## Evidence

Produce the artifacts required to test the completion claim. Record skipped checks and limitations.

## Review

Inspect the exact output against the contract. Depending on the Level, review may be human inspection, a separate model context, deterministic validation, or a combination.

## Acceptance

The named authority accepts, revises, defers, or rejects the result. A work-complete claim is not automatically an acceptance decision.

## Memory update

Update project state only after the accepted result is integrated. Promote reusable learning into its canonical home and archive temporary state that no longer routes future work.

