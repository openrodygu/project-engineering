# Pull requests

A pull request says: "Here is a change on a branch. I propose we merge it. Please review it first."

It is a proposal, not a demand. The reviewer's job is to help it land safely.

## Keep it small

A good PR does one thing. Small changes get better reviews, fail less often, and are easier to revert.

A rough guide:

- Under 400 changed lines is easy to review.
- 400–1,000 needs a clear description and a reason to stay together.
- Over 1,000 should usually be split unless it is generated or mechanical.

If a change cannot be small, say why in the description.

## The description

Use the same five sections every time:

```markdown
## What changed
Add null handling to the payroll export.

## Why
The export crashes when a user has no employee ID.
Fixes #142.

## How to test
1. Create a user without an employee ID.
2. Run the export.
3. Confirm the file downloads with an empty ID column.

## Risk
Low. The change only affects the export path. I ran the export
tests and one manual check.

## Notes
I did not change the UI or the API contract.
```

A reviewer should be able to start from this without asking what the PR is for.

## Draft early if it helps

Open a draft PR when you want early feedback on direction. Say what is still missing. Do not mark it ready until the description is accurate and the tests pass.

## Respond to review

- Reply to each comment, even if only "done".
- Push fixes to the same branch.
- Do not force-push while someone is reviewing unless you warn them.
- If you disagree, explain the constraint and ask for a decision.
- Keep the conversation about the code, not the person.

## Before you request review

- The diff contains only intended changes.
- Tests pass, or you explain why they do not.
- The description matches the final diff.
- No debug code, secrets, or unrelated formatting.
- Someone else can run or verify the change.

## Try it

Write a PR description for a change you made recently, even if it is already merged. Use the five sections. Then ask: could a reviewer start without asking me a question?

Next: [04 Code review](04-code-review.md)
