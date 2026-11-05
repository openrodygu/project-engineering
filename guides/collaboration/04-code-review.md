# Code review

A code review checks whether a change is correct, safe, and understandable. It is not a test of the author's worth.

## What to look for

Start with the high-impact questions:

1. **Does it solve the stated problem?** The description and the diff should agree.
2. **Is it correct?** Check edge cases, error paths, and assumptions.
3. **Is it safe?** Look for secrets, injection, data loss, and permission gaps.
4. **Is it tested?** Tests or manual steps should cover the change.
5. **Is it readable?** Names, structure, and comments should help the next reader.
6. **Is it in scope?** Unrelated edits make the review harder and the history noisy.

Style is worth mentioning, but only after correctness and risk.

## Label your comments

Clear labels make a review easier to act on:

- **Blocking** — must be fixed before merge.
- **Suggestion** — a better option, not required.
- **Question** — you need context before deciding.
- **Nit** — small preference; fine to ignore.

Example:

```text
Blocking: this path returns null when the list is empty,
but the caller expects an array. Can we return []?
```

That is more useful than "this is wrong".

## Review the change, not the person

- Ask about the code, not the author's skill.
- Explain the risk, not just the rule.
- Offer a concrete alternative when you can.
- Say when something is good. Reviews that only list problems wear people down.
- If a comment would take more than a few paragraphs, move to a call.

## Turnaround

A review is part of the work, not an interruption. Aim for a first response within one working day on normal changes. If you cannot get to it, say so and give a time.

Do not approve a change you do not understand. "Looks fine" on a risky diff is worse than a slower review.

## When you disagree

State the tradeoff. Ask which constraint matters most. If you still disagree, let the maintainer decide and write the decision down. A merged change with a recorded tradeoff is better than a long unresolved thread.

## Try it

Take a small diff — yours or a public one — and review it with the six questions above. Label at least three comments as Blocking, Suggestion, or Nit. Then rewrite one comment to name the risk and a concrete fix.

Next: [05 Communication standards](05-communication-standards.md)
