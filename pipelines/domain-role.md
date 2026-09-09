# Domain role pipeline

Create a durable role by building its knowledge and artifact contract—not by assigning a persona name.

## 1. Identify a recurring knowledge gap

Write the questions that the main workflow repeatedly answers poorly or routes inconsistently. A one-time question usually needs research, not a permanent role.

## 2. Define the mandate

Specify:

- recurring decisions the role supports;
- inputs it may inspect;
- outputs it must produce;
- what remains outside its scope;
- whether it recommends or decides;
- where it escalates uncertainty.

Start from [Role contract](../templates/role-contract.md).

## 3. Research the domain

Send the role to primary and authoritative sources first. Every durable claim should retain enough source information to verify it later.

Use the [Research pipeline](research.md) for each bounded research question. The role’s knowledge base is built from reviewed research artifacts, not from an unrecorded browsing session.

Separate:

- established domain knowledge;
- current or time-sensitive facts;
- project-specific assumptions;
- the role’s own inference.

## 4. Build the knowledge base

Store reusable findings in `knowledge_base/` and route them through an index. Do not paste entire sources. Record concise claims, applicability, provenance, and uncertainty.

## 5. Produce a first project report

Test the role on a real decision. The report must reference the project state examined and apply the knowledge base to a bounded question.

Use [Domain report](../templates/domain-report.md).

## 6. Validate usefulness

Keep the role only if its report changes a decision, identifies a real risk, or gives repeatable evaluation criteria. A role that merely restates the main session adds ceremony.

## 7. Connect it to routing

Define:

- which task signals invoke the role;
- who consumes its report;
- whether another authority must synthesize disagreements;
- what the role must never approve.

## 8. Maintain the boundary

Project reports do not automatically enter the knowledge base. Promote a finding only when it is reusable, supported, and owned. Retire knowledge when newer evidence supersedes it.
