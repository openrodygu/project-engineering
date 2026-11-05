# Documentation and decisions

Documentation is how a team avoids re-solving the same problem. Decisions are the most valuable docs because they explain why the code looks the way it does.

## The three docs most teams need

1. **README** — what this is, how to run it, and where to get help.
2. **How-to notes** — the few procedures people repeat, such as local setup or release steps.
3. **Decision records** — the choices that would be expensive to reverse.

You do not need a documentation site. A folder of short Markdown files is enough.

## Write a decision record

Keep it to one page:

```markdown
# Use a single shared team vault

## Date
2026-11-04

## Context
Team status was spread across chat, spreadsheets, and personal lists.

## Options
1. Keep the current tools.
2. Use one team vault with dotpm.

## Decision
Adopt one team vault for shared status. Personal planning stays
in each person's own vault.

## Consequences
- The team can see status in one place.
- Someone must keep the vault current.
- Personal notes do not become team commitments by accident.

## Owner
Alex
```

The value is in the **Context**, **Options**, and **Consequences** sections. They let a future reader understand the tradeoff, not just the outcome.

## Where docs live

- **In the repository** for setup, architecture, and decisions.
- **In the team vault** for project status, deliverables, and shared context.
- **In the personal vault** for your own notes and drafts.

Do not duplicate the same document in several places. Pick one authoritative location and link to it.

## Keep docs alive

- Update the README when setup changes.
- Add a decision record when a choice would surprise someone later.
- Delete or archive docs that are no longer true.
- Put the date on anything that goes stale.

A short doc that is current beats a long doc nobody trusts.

## Try it

Write a decision record for a choice you made in the last month. Include at least two options and one consequence you did not like. Put it in the repository or team vault and link it from the relevant issue or project note.

Next: [07 Working with non-engineers](07-working-with-non-engineers.md)
