# Communication standards

A shared standard for commits, pull requests, and review comments makes history searchable and decisions easier to revisit. Keep the standard short enough that people actually use it.

## Commit messages

Use a consistent format so the history reads like a log of intent.

Format: `[<type>](<scope>): <subject>`

| Type | Purpose | Example |
| --- | --- | --- |
| feat | New functionality | `[feat](user): add two-factor authentication` |
| fix | Bug fix | `[fix](api): handle missing user ID in payroll` |
| refactor | Code change with no behavior change | `[refactor](ui): simplify sidebar structure` |
| docs | Documentation | `[docs]: update deployment instructions` |
| test | Tests | `[test](auth): cover token expiration` |
| chore | Maintenance | `[chore]: upgrade webpack to v5` |

Write the subject in the imperative mood: "add", "fix", "remove". Keep it under about 70 characters. Put the reason in the body when it is not obvious.

## Pull request descriptions

A pull request is a proposal: "I finished work on my branch and propose that it merge. Please review it first."

A good description lets a reviewer start without asking basic questions. It covers:

- **What changed** and where.
- **Why** — the problem or goal, with a link to the issue.
- **How to test** — exact steps.
- **Risk** — what could break and what you checked.
- **Related work** — tickets, designs, or decisions.

## Scenario-based detail

Add the section that matches the change.

### New feature

- **What** — the functional scope. What does the user see or what does the code do?
- **Why** — the business or user problem. Example: "Users lose drafts when they switch devices."
- **How** — the technical approach. Example: "Add a draft store, update `DraftService`, and expose `/v1/drafts`."

### Bug fix

- **Diagnosis** — the observed failure.
- **Root cause** — why it failed. Example: "The code assumed a user ID was always present, but the API can send null."
- **Fix** — the specific change. Example: "Add a null check and a safe default."

### Refactor

- **Why** — why the structure needed to change.
- **What** — the scope of the cleanup.
- **Impact** — any public API change. If none, say "No observable behavior change."

## Review comments

- Be specific: name the line, the risk, and a possible fix.
- Label comments as Blocking, Suggestion, Question, or Nit.
- Ask before assuming intent.
- Keep one idea per comment.
- Move long debates to a call and write the result in the PR or decision record.

## Plain language

Write for a reader who has the code but not your context.

- Prefer short sentences.
- Define acronyms on first use.
- Say what happens, not just what changed.
- Use the same words for the same thing.

## Try it

Take a vague review comment such as "this seems wrong" and rewrite it three ways:

1. As a Blocking comment with the risk and a fix.
2. As a Question that asks for context.
3. As a Suggestion with a concrete alternative.

Then use one of them in your next review.

Next: [06 Documentation and decisions](06-documentation-and-decisions.md)
