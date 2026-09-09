# Failure story — review that judged someone else’s work

## What happened

Several sessions shared one working copy of the project. When a run created its own work line, it moved every session in that copy onto it, and changes authored by the other sessions were carried into the run’s landing.

Review was scoped as the difference between two points in project history. It therefore inspected those foreign changes as if the run had produced them. The findings were reported against the run, and a repair contract sent an Executor to fix a file the run had never touched.

## Why the workflow missed it

- the review scope was a range of history rather than the set of changes the run actually authored;
- the workspace was shared, so “current state” was not private to the session reading it;
- every session acted under the same recorded identity, so the check for a foreign author could not fail — a guard that cannot fail is not a guard;
- nothing in the output looked wrong. The findings were real defects in real files sitting on the run’s own landing. Only the attribution was false.

## Change introduced

- scope review by the identifiers of the changes under review, not by a range between two points;
- verify authorship before landing, and treat a foreign change inside a landing as a stop rather than a finding;
- give concurrent sessions isolated working copies wherever the tool allows it;
- where isolation is unavailable, treat concurrency as an explicit routing decision with a named landing order, not as free speed.

## Principle earned

> A failure with no symptom is found by scope, not by noticing.
