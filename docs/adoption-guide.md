# Adoption guide

Adopt one complete Level, then add specialized pipelines only when the output requires them. Do not copy the entire repository into every project.

## Step 1 — Choose the work, then the Level

Name the concrete workstream or task. Choose its Level using [Choosing a level](choosing-a-level.md). A project may use different levels for different work.

## Step 2 — Create only the required artifacts

### Level 1

Required:

- one Task Brief, which may live in the prompt or as a file.

### Level 2

Required:

- project instructions;
- `CURRENT_STATE.md`;
- Task Brief;
- durable decision records when needed.

### Level 3

Required:

- canonical project map or instructions;
- current state;
- Task Contracts;
- review findings;
- decision and approval records;
- role homes for any persistent domain roles.

### Level 4

Required:

- the complete Level 3 contract;
- run objective and budget;
- eligible-task rules;
- escalation and stop policy;
- per-task evidence and landing state;
- final run report.

## Step 3 — Assign canonical homes

For every live artifact type, record:

- its path;
- its owner;
- who reads it;
- when it changes;
- where old versions go.

The same template may be referenced by several levels, but the project should not maintain several editable copies of the same fact.

Then define model and context routing by responsibility. Do not bind an entire project or Level to one configuration. Start with [Model and context routing](../components/model-and-context-routing.md) and keep the policy as small as the work permits.

## Step 4 — Add pipelines by output type

- recurring domain gap: [Domain role](../pipelines/domain-role.md);
- one bounded external question: [Research](../pipelines/research.md);
- bounded general work: [Standard task](../pipelines/standard-task.md);
- generated visual material: [Visual assets](../pipelines/visual-assets.md);
- precision visual implementation: [Mock to implementation](../pipelines/mock-to-implementation.md).

A pipeline is optional. It is not a new Level.

## Step 5 — Test the lifecycle with one task

Before scaling:

1. run one real task;
2. resume it in a fresh session if the Level promises continuity;
3. verify that every required file has one owner;
4. demonstrate that the completion check detects a relevant failure;
5. record where the human must intervene;
6. remove artifacts that were never used.

Use the [Setup checklist](setup-checklist.md) for a final audit. A filled [sample workspace](../examples/sample-workspace/README.md) demonstrates the same contracts in context.

## Step 6 — Increase complexity only after an observed failure

Do not add Autopilot because the diagram looks complete. First make the Level 3 loop reliable by hand. Automating an unclear process makes its ambiguity faster.

## Minimal project map

```text
project/
├── PROJECT.md             # intent and durable constraints
├── CURRENT_STATE.md       # current position and routing
├── tasks/                 # bounded work contracts
├── decisions/             # durable decisions
├── approvals/             # explicit human gates
├── evidence/              # task evidence and review
└── roles/                 # only persistent roles that own knowledge
```

This is an example, not a required naming convention. Preserve the ownership model even when your existing tools use different paths.
