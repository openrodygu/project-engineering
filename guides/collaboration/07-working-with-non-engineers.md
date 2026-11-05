# Working with non-engineers

Most collaboration problems are translation problems. The engineer knows the constraint. The stakeholder knows the outcome they need. Neither can see the other's side without help.

## Start with the decision

Ask what the other person needs to decide or do. Then give them the smallest amount of technical detail that supports it.

A useful structure:

1. **What this means for you** — the impact in their terms.
2. **What we know** — the facts, without jargon.
3. **What we do not know** — the open questions.
4. **What happens next** — who does what, and when.

## Drop the jargon

Translate without being condescending:

| Instead of | Say |
| --- | --- |
| "The race condition causes intermittent failures." | "Two actions can collide and sometimes lose data. We are making them take turns." |
| "We need to refactor the service." | "We need to clean up this part before adding the new feature, or each change will get slower." |
| "The migration is blocked on schema changes." | "We cannot move the data until the new fields exist. That work is scheduled for Tuesday." |

If a term is necessary, define it once and use it consistently.

## Use artifacts

A screenshot, a short demo, or a one-page diagram ends more debates than a long thread. Show the thing working, or show the exact error.

When you cannot show it, describe the user's experience step by step. "You click Save, wait ten seconds, and see an error" is clearer than "the endpoint times out".

## Set expectations honestly

- Say when you are unsure.
- Give a range, not a false exact date.
- Name the tradeoff when there is one.
- Tell people early when something slips.

Bad news early is a planning input. Bad news late is a surprise.

## Write it down

After a meeting with a stakeholder, send a short summary: what was decided, what is next, and who owns it. This prevents the "I thought you meant..." problem.

## Try it

Take a recent technical update and rewrite it for a non-engineer in five sentences:

1. What it means for them.
2. What changed.
3. What is still uncertain.
4. What you need from them.
5. What happens next.

Read it aloud. Remove any sentence that only makes sense to another engineer.

Next: [Back to the Collaboration skill](README.md)
