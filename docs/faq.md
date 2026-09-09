# Frequently asked questions

## Is this a tool?

No. It is a documentation-first reference implementation: operating Levels, canonical components, specialized pipelines, templates, and filled examples. You can apply it with the AI tools and file layout you already use.

The readable artifacts are the interface. There is no required installer, runtime, command vocabulary, or vendor.

## Is documentation useful without automation?

Yes, when the documents define executable behavior rather than merely describe ideas. A task contract can block work that is not ready. An approval record can prevent inferred consent. An evidence bundle can expose a false completion claim. A role contract can determine where research and reports live.

These artifacts are meant to be copied, filled, inspected, and changed. Automation may later enforce them, but it is not what makes them operational.

## Must I adopt the whole repository?

No. Choose one Level and copy only its required artifacts. Add a specialized pipeline only when the output needs it.

## Are the Levels a maturity ladder?

No. They are independent operating configurations. Level 4 is not inherently better than Level 1; it pays more coordination cost to control a different failure surface.

One dependency is real, and it is mechanical rather than developmental: Level 4 automates the Level 3 loop, so it needs that loop to work by hand first. Everything else about the levels is a free choice per task or workstream.

## Can one project use several Levels?

Yes. Select a Level per task or workstream. A routine edit may use Level 1 while a consequential multi-domain change in the same project uses Level 3 or 4.

## Does a higher Level require a stronger model?

No. Workflow control and model capability are separate axes. Route models by responsibility, ambiguity, context breadth, risk, and verifiability. See [Model and context routing](../components/model-and-context-routing.md).

## Why use files when AI tools already retain chat history?

Chat history preserves conversation; it does not automatically establish ownership, freshness, authority, or canonical truth. Files make those boundaries inspectable and portable across sessions and tools.

## Why not load every file into every session?

More context is not the same as correct context. Each responsibility should start from a small routing artifact and load the smallest complete set of owned sources.

## Is a role just a specialized prompt?

Not here. A durable role has a mandate, input contract, output contract, owned knowledge base, report home, and authority boundary. A persona without ownership is temporary behavior, not project architecture.

## Do several reviewers provide independent proof?

Not automatically. Separate contexts can reduce author bias, but similar models may reproduce the same mistake. Review needs distinct lenses, primary artifacts, deterministic checks where possible, and a human gate where judgment or accountability requires one.

## Is pixel comparison enough for visual implementation?

No. Pixel and regional diffs are useful evidence, but they can pass or fail for the wrong reasons. Pair them with geometry probes, deterministic rendering controls, semantic and interaction checks, tolerances, and human judgment. See [Mock to implementation](../pipelines/mock-to-implementation.md).

## Can an orchestrator approve its own work?

Only if the authority map explicitly grants that decision—and high-impact acceptance normally should remain elsewhere. Autonomy advances through predeclared gates; it does not imply unlimited authority.

## Is this workflow claimed to be unique?

No. Several public methods share parts of it. This repository documents one working system, including its history, visual pipelines, role knowledge architecture, evidence rules, and failure-driven evolution. See [Related work](related-work.md).

## Where should I start?

For one bounded task, start at [Level 1](../levels/1-focused-session.md). If work must survive sessions, start at [Level 2](../levels/2-resumable-project.md). Move to separated roles or autonomy only when their controls address an observed problem.
