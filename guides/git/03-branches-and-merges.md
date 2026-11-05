# Branches and merges

Use branches to keep experiments separate, then merge them when they are ready.

## What a branch is

A branch is a movable label on a commit. Creating one is cheap: Git writes a new pointer. Switching branches changes which snapshot is in your working tree.

```sh
git branch              # list branches
git switch -c add-notes # create and switch
git switch main         # switch back
git branch -d add-notes # delete after merge
```

`git switch` is the modern command. `git checkout` still works and does more, but `switch` is clearer for branches.

## The normal loop

1. Start from an up-to-date main.
2. Create a branch with a descriptive name.
3. Make small commits.
4. Merge the branch back when it is ready.
5. Delete the branch.

```sh
git switch main
git pull
git switch -c fix-login-timeout
# edit, add, commit
git switch main
git merge fix-login-timeout
```

If you do not have a remote yet, skip `git pull`. It is only there to update from a shared copy.

## Fast-forward and three-way merges

- **Fast-forward** — main has not moved since you branched, so Git just moves the label forward. No merge commit.
- **Three-way merge** — both branches have new commits, so Git creates a merge commit with two parents.

Both are normal. A fast-forward keeps history linear. A merge commit records that a branch existed. Teams choose based on what they want history to show.

To keep a merge commit even when a fast-forward is possible:

```sh
git merge --no-ff add-notes
```

To keep history linear instead, rebase your branch onto main before merging. Rebase rewrites commits, so only do it on branches nobody else is using.

## Merge versus rebase

| Merge | Rebase |
| --- | --- |
| Preserves the real branch history | Produces a straight line |
| Adds a merge commit | Rewrites commit IDs |
| Safe on shared branches | Best for local, unshared work |

Use merge for shared branches. Use rebase to tidy your own branch before review, if the team agrees.

## When to branch

Branch when the change is not ready for the main line:

- A feature that takes more than a few minutes.
- A fix that needs testing.
- An experiment you may throw away.
- A release you need to stabilize.

Do not branch for a one-line typo if your team works directly on main. Adopt the smallest workflow that fits the risk.

## Try it

Practice the full loop.

1. From `main`, create a branch called `add-notes`.
2. Add a section to a file and commit.
3. Switch back to `main` and confirm the change is not there.
4. Merge `add-notes` into `main`.
5. Delete the branch and run `git log --oneline --graph`.

Work in `local-project/source/`.

Next: [Conflicts](04-conflicts.md)
