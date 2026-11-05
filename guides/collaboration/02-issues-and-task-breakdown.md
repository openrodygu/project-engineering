# Issues and task breakdown

An issue is a conversation and a small commitment. It records what needs doing, why it matters, and what "done" means.

## What a useful issue contains

- **Context** — the situation and who is affected.
- **Problem** — what is wrong or missing.
- **Expected result** — what should be true when it is done.
- **Acceptance criteria** — how someone will check it.
- **Constraints** — deadlines, compatibility, or things not to change.
- **Links** — related issues, designs, logs, or decisions.

A title should name the outcome, not the activity. "Login fails for users without an email" is easier to act on than "Fix login".

## Break work into reviewable pieces

A task is the right size when one person can finish it and someone else can review it without a long meeting. A useful rule: if it takes more than about three days, split it.

Split by outcome, not by layer:

```text
Too big:  Add user profile editing
Better:   Add profile edit form
          Save profile changes to the API
          Show validation errors
          Add tests for profile update
```

Each piece should be independently understandable. If every piece depends on every other piece, the breakdown is not helping yet.

## Acceptance criteria

Write criteria as observable facts:

```text
- A user can open their profile and see current values.
- Saving a valid change updates the stored record.
- An invalid email shows a field-level error.
- The existing login flow still works.
```

Avoid "works correctly" or "improved". Those cannot be checked.

## Issues are not status reports

Use comments for new information and decisions. Update the issue when the scope changes. Close it when the work is done or deliberately dropped. Do not leave a stale issue open for months with no owner.

If an issue becomes a team commitment, mirror it in the team vault. The issue holds the technical detail; the vault holds the team's shared view.

## Try it

Take a vague request, such as "the dashboard is slow", and turn it into an issue with:

- Context and the affected user.
- One measurable expected result.
- Three acceptance criteria.
- Three subtasks that can be reviewed separately.

Then decide which one you would do first and why.

Next: [03 Pull requests](03-pull-requests.md)
