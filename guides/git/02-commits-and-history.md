# Commits and history

Make each commit tell one clear story, then use history to understand what changed.

## Commit small and complete

A good commit does one thing. It may touch several files, but they belong to the same change.

- **Atomic** — the project still makes sense after the commit.
- **Complete** — tests and related docs move with the code.
- **Bounded** — you can describe it in one sentence without "and".

Small commits are easier to review, revert, and understand. A 2,000-line commit is not a unit of work; it is a filing cabinet.

## Write a useful message

Use a short subject line, then a body when the reason is not obvious.

```text
Add vendor comparison table

The brief needs a side-by-side view of the three vendors.
Figures come from the March quotes.
```

Rules that work:

- Subject in the imperative: "Add", "Fix", "Remove", not "Added" or "Fixes".
- Keep the subject under about 50 characters.
- Explain why, not just what. The diff already shows what changed.
- Reference the issue or task when one exists.

"Update stuff" is not a message. "Fix login timeout for slow networks" is.

## Read history

```sh
git log --oneline
git log --oneline --graph --all
git show <commit>
git diff <old>..<new>
git blame file.txt
```

- `log` shows the sequence of commits.
- `show` displays one commit and its diff.
- `diff A..B` shows what changed between two points.
- `blame` shows which commit last touched each line.

Use history to answer questions: When did this change? What else moved with it? Who knows about it? That is more useful than assigning fault.

## Find a change

```sh
git log --grep="vendor"
git log -S "timeout" --oneline
```

`--grep` searches messages. `-S` finds commits that added or removed a string. Both are faster than scrolling.

## Keep history honest

- Do not rewrite commits that others have already pulled unless the team agrees.
- Do not commit generated files, secrets, or local settings.
- Do not mix formatting changes with behavior changes. Reviewers cannot see the real change through the noise.
- Amend only your own unpushed commit.

## Try it

Create three commits that tell a story.

1. Add a file with one paragraph and commit it.
2. Add a second section in a separate commit.
3. Fix a typo in a third commit.
4. Run `git log --oneline` and `git show` on the middle commit.
5. Rewrite one vague message with `git commit --amend` before pushing.

Work in `local-project/source/`.

Next: [Branches and merges](03-branches-and-merges.md)
