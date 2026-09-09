# Visual asset index

| Asset ID | Purpose | Status | Approved file and hash | Source or generation record | Dimensions and variants | Approval | Replaces |
|---|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |  |

## Status values

- `DRAFT` — brief exists; no candidate is valid for use.
- `CANDIDATE` — available for review; not approved for project use.
- `APPROVED` — may be used within the recorded boundary.
- `REJECTED` — must not re-enter through search or agent suggestion.
- `RETIRED` — previously approved but superseded or no longer valid.

## Invariants

- A candidate does not become approved because it was generated successfully.
- Material edits to an approved asset create a new candidate or version.
- Rejected and retired files remain clearly distinguishable from approved files.
- Each approved entry links to an explicit approval record.
