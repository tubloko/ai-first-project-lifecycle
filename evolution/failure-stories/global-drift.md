# Failure story — local correctness, global drift

## What happened

Each implementation task was locally reasonable. Small compromises entered the project, and later decisions treated those compromises as the new starting point. Over many iterations, the project became internally coherent but moved away from its original intended reality.

## Why the workflow missed it

- reviewers checked task compliance more often than project intent;
- future work was derived from current implementation;
- missing states and transitions were difficult to see in isolation;
- local improvements produced no obvious failing test.

## Change introduced

Before implementation, the affected surface must have an explicit model of intended rules, states, transitions, and constraints. Visual states are modeled in mocks where useful. Tasks derive from that intended reality rather than only from current output.

## Principle earned

> Local correctness does not protect global intent.

