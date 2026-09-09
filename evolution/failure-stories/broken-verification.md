# Failure story — a verifier that did not prove its claim

## What happened

A verification path produced a successful result while skipping or miscounting required work. In another case, a visual metric confidently reported differences that were caused by incompatible rendering assumptions rather than by the implementation defect the gate was intended to detect.

## Why the workflow missed it

- success accounting counted attempted steps rather than successful outputs;
- stale generated artifacts were mixed with the current run;
- return codes and empty outputs were not always validated;
- the verifier had not been tested against a known defect;
- one metric was asked to stand in for semantic correctness.

## Change introduced

- fail closed on missing inputs, fonts, empty artifacts, and failed commands;
- track outputs produced by the current run;
- demonstrate that the verifier detects a relevant failure;
- separate pixel, geometry, semantic, deterministic, and human checks;
- report blind spots explicitly.

## Principle earned

> A check that cannot fail is decoration.

