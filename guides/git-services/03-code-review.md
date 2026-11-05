# Code review

Improve the change and share context, without turning the review into a gatekeeping ritual.

## What review is for

A review checks three things:

- **Correctness** — does the change do what it says?
- **Clarity** — can the next person understand it?
- **Risk** — what could break, and is that acceptable?

Review is not a test of the author's worth. It is a conversation about the change. Keep it specific and kind.

## Before you ask for review

The author should:

- Keep the pull request small and focused.
- Write the description with What, Why, and How to check.
- Run the tests and checks locally.
- Remove debug code and unrelated edits.
- Link the issue.
- Say what feedback they want: design, naming, edge cases, or a final check.

A prepared pull request gets a better review. A vague one gets a shrug.

## As a reviewer

1. Read the description and linked issue first.
2. Look at the change as a whole before reading line by line.
3. Check the tests. Do they cover the risk?
4. Run the change if it is easy to do so.
5. Ask questions where context is missing.
6. Separate blocking issues from suggestions.
7. Approve, or request changes with a clear reason.

A useful comment says what and why:

- Weak: "This is wrong."
- Strong: "This retries forever when the service is down. Should we cap it at three attempts?"

## Review checklist

- Does the change match the issue and the description?
- Is there a test for the new behavior or the fixed bug?
- Are error paths handled?
- Are names clear without extra comments?
- Is anything unrelated included?
- Are secrets, tokens, or personal data exposed?
- Do the docs need an update?
- Is the change safe to roll back?

You do not need every item on every review. Use the list when you are unsure.

## Tone and turn-around

- Comment on the code, not the person.
- Say "we" when it is a team convention.
- Mark non-blocking ideas as suggestions.
- Ask before assuming.
- Review within one working day when you can. A blocked author is expensive.
- If you cannot review, say so and suggest someone else.

## Resolve and merge

The author responds to every blocking comment, either with a change or with a reason. Then the reviewer approves.

Merge when:

- The checks pass.
- The blocking comments are resolved.
- The description is still accurate.
- The branch is up to date with the target.

## Try it

Review one pull request.

1. Open a pull request from your repository or a public project.
2. Read the description and the diff.
3. Leave one specific, non-blocking suggestion.
4. Leave one question about a risk or an edge case.
5. Decide whether you would approve, and write one sentence explaining why.

Do this on GitHub. In the workspace map, this is the `hosted-service/` part.

Next: [CI and checks](04-ci-and-checks.md)
