# Role architecture

A role is a durable responsibility boundary, not a character description.

## Role contract

Every persistent role should define:

- mandate: the recurring question it exists to answer;
- inputs: which project artifacts and sources it may use;
- owned knowledge: what belongs in its knowledge base;
- outputs: the artifacts it must produce;
- authority: what it may recommend, decide, change, or approve;
- escalation: when and where it must stop;
- home: the canonical folder for its knowledge and reports.

## Suggested folder contract

```text
roles/<role>/
├── ROLE.md
├── knowledge_base/
│   ├── INDEX.md
│   └── <reusable-domain-knowledge>.md
└── reports/
    └── YYYY-MM-DD-<question>.md
```

### `knowledge_base/`

Contains reusable domain knowledge supported by named sources. It should survive individual project questions.

### `reports/`

Contains dated analysis of a specific question against a specific project state. A report may cite the knowledge base, but it does not silently rewrite it.

## Creating a role

Do not create a role merely because a name sounds useful. Create one when:

- the same domain question recurs;
- the question needs sources or evaluation criteria not carried by the main session;
- a distinct report improves decisions;
- the role can own knowledge without duplicating another role;
- its authority boundary can be stated clearly.

Use the [Domain role pipeline](../pipelines/domain-role.md) to bootstrap it.

## Reports are the interface between roles

Roles should not depend on private conversational memory. A report records:

- the question;
- state examined;
- sources;
- findings;
- recommendation or verdict;
- uncertainty;
- authority limit;
- next recipient.

## Avoid role theater

Warning signs:

- several roles read the same inputs and produce interchangeable opinions;
- a role has no owned files;
- a role’s conclusion cannot be traced to evidence;
- a title implies authority that the contract does not grant;
- adding roles increases agreement but not coverage.

