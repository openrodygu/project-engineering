# Knowledge and decisions

Capture the reasoning behind important choices so the team can revisit, defend, or change them later.

## Why this matters

Projects outlive the people who started them. A recorded decision lets a new team member understand why the system looks the way it does, trace a failure back to the problem it solved, and revisit the choice when the problem changes.

The cost is small: a short note written while the reasoning is fresh.

## Decision records

An Architecture Decision Record (ADR) is a short Markdown file that captures one significant decision, its context, and its trade-offs.

Use one when the team chooses between high-level options, such as a data store, a service boundary, or a storage format. Write one when the decision is expensive to reverse or likely to be questioned later.

### ADR structure

| Section | Goal | What to write |
| --- | --- | --- |
| Title | Identify the decision | `ADR-001: Use one file per task` |
| Status | Track its state | Proposed, Accepted, Superseded, Obsolete |
| Context | State the problem | What forced a decision? What constraints applied? |
| Decision | State the choice | What we will do, in one or two sentences. |
| Consequences | State the trade-offs | What gets better, what gets worse, what we accept. |
| Related | Cross-reference | Links to related decisions and notes. |

Example:

```markdown
# ADR-001: Use one file per task

**Status:** Accepted
**Date:** 2026-03-01

## Context

The team needs shared task visibility. Two people editing one board at once
would create conflicts. Tasks should also be searchable outside the app.

## Decision

Store each task as its own Markdown file with metadata in properties.

## Consequences

- Smaller diffs and fewer sync conflicts.
- Tasks are searchable and editable without the app.
- More files to manage; the index must be rebuilt after manual moves.
```

A decision log is the index: one line per ADR with its number, title, status, and date. Keep it next to the ADRs so people can find the set.

## Capture knowledge as you go

Write the reason, not just the result. Link the note to the task it affects, record the date and the people involved, and mark old decisions as superseded instead of deleting them.

## Code ownership map

Maintain a living note that maps key components to responsible teams or people. It prevents bottlenecks and makes accountability visible.

| Area | Owner | Backup |
| --- | --- | --- |
| Shared vault schema | Alice | Bob |
| Release process | Carol | Dave |
| Vendor integration | Bob | Alice |

Update it when ownership changes. An out-of-date map is worse than none.

## Try it

Write one decision record and one ownership entry.

1. Pick a real decision from your project.
2. Fill in the ADR sections, including two consequences.
3. Add the one-line entry to your decision log.
4. Add one row to the ownership map.

Store them in `local-project/pm-vault/`.

Next: [Execution and metrics](08-execution-and-metrics.md)
