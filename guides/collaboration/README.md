# Collaboration

Work with other people on a shared repository without losing context, decisions, or goodwill.

## Do this now

20–30 minutes. You will finish with a pull-request description and a review checklist.

1. Open a repository you work in. If you do not have one, read [Git services](../git-services/) and create a practice repository.
2. Pick a small change: a bug fix, a docs correction, or a one-file improvement.
3. Write a pull-request description with these sections:
   - **What changed** — one or two sentences.
   - **Why** — the problem or goal.
   - **How to test** — exact steps.
   - **Risk** — what could break and how you checked.
4. Write a review checklist with these items:
   - The change does one thing.
   - The description matches the diff.
   - Tests or manual checks cover the change.
   - Names and structure are readable.
   - No secrets, debug code, or unrelated edits.
   - Docs or decisions are updated if behavior changed.
5. Save both in a note or in your project folder.

You now have the artifact: a PR description and a review checklist you can reuse.

## What it is

A shared repository is a conversation with history. Issues record what needs doing and why. Pull requests propose a change. Reviews check the change before it lands. Commit messages preserve the reasoning for later.

Collaboration is a practice, not a gate. The goal is to help the change land safely and to leave the next reader with enough context.

## Go deeper

1. [01 Shared repo](01-shared-repo.md)
2. [02 Issues and task breakdown](02-issues-and-task-breakdown.md)
3. [03 Pull requests](03-pull-requests.md)
4. [04 Code review](04-code-review.md)
5. [05 Communication standards](05-communication-standards.md)
6. [06 Documentation and decisions](06-documentation-and-decisions.md)
7. [07 Working with non-engineers](07-working-with-non-engineers.md)

## Where this fits

- Hosted repository: `hosted-service/`
- Hosted repository mechanics: [Git services](../git-services/)
- Shared task view: `local-project/pm-vault/`
For the system view, read the [Handbook](../../handbook/README.md).

## Common mistakes

- **Giant pull requests.** A 2,000-line PR gets a shallow review. Keep changes to one purpose.
- **Empty descriptions.** Reviewers cannot review intent they cannot see.
- **Reviewing style only.** Correctness, risk, and tests matter more than personal preference.
- **Arguing in comments.** Move a long disagreement to a call, then write the decision down.
- **Skipping the issue.** A PR with no stated problem is hard to judge.

## Next skill

Read [Git services](../git-services/) for the hosted-repo mechanics, or [Team lead](../team-lead/) if you also lead the people doing the work.
