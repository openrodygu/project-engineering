# Undoing and hygiene

Recover from mistakes without losing work, and keep the repository clean enough to trust.

## First, check where you are

Before changing history, run:

```sh
git status
git log --oneline -5
```

Know what is committed, what is staged, and what is only in the working tree. Most panic comes from skipping this step.

## Restore a file you edited

Discard unstaged changes to one file:

```sh
git restore path/to/file
```

Restore a staged file to unstaged while keeping the edit:

```sh
git restore --staged path/to/file
```

These commands overwrite local changes. Be sure the edit is not worth keeping.

## Undo a commit

- **Keep the changes, move the branch back:**

  ```sh
  git reset --soft HEAD~1
  ```

- **Keep the changes unstaged:**

  ```sh
  git reset HEAD~1
  ```

- **Discard the commit and its changes:**

  ```sh
  git reset --hard HEAD~1
  ```

`--hard` deletes work. Use it only when you are sure, and never on a branch others have pulled.

## Undo a pushed commit safely

Use `revert` on shared history. It creates a new commit that reverses an earlier one, so nobody else's history is rewritten.

```sh
git revert <commit>
git push
```

This is the safer choice for main and any branch other people use.

## Recover with reflog

`reflog` records where your branch and HEAD have been. It can rescue a commit you thought was lost.

```sh
git reflog
git reset --hard HEAD@{2}
```

The reflog is local and temporary. Do not treat it as a backup, but it is excellent for the last few mistakes.

## Amend and stash

Fix the last commit message or add a forgotten file:

```sh
git add forgotten.txt
git commit --amend
```

Amend only commits you have not pushed.

Set work aside without committing:

```sh
git stash
git stash list
git stash pop
```

Stashes are easy to forget. Use them for minutes or hours, not weeks.

## Keep the repository clean

- Commit only source and intentional files.
- Add build output, dependencies, logs, and secrets to `.gitignore`.
- Never commit `.env` files or tokens. If you do, rotate the secret; deleting the file is not enough.
- Remove merged branches locally.
- Run `git fetch --prune` so stale remote branches disappear.
- Do not commit large binaries when a link or a release asset will do.

## Try it

Practice recovery in `local-project/source/`.

1. Make a commit, then undo it with `git reset --soft HEAD~1`.
2. Commit again, then revert it with `git revert`.
3. Make a commit, reset hard, and find it again with `git reflog`.
4. Add a `.gitignore` entry for a file you do not want tracked.
5. Run `git status` and confirm the tree is clean.

Next: [Git services](../git-services/README.md) — publish the repository and collaborate.
