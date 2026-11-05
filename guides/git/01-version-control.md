# Version control

Understand what Git is tracking and why the staging area exists.

## The problem Git solves

Without version control, history lives in filenames: `report-final-v2`, `report-final-v2-really`, `report-final-good`. Nobody knows which one is current, and nobody can tell what changed between them.

Git records snapshots over time. You can see what changed, when, by whom, and why. You can go back to an earlier state without keeping copies of the whole folder.

## The three states

- **Working tree** — the files on disk. You edit here.
- **Staging area** — the changes you have selected for the next commit.
- **Repository** — the stored history of commits.

The staging area is the part that confuses people. It exists so you can commit a coherent change even when the working tree contains unrelated edits. You stage the files that belong together, then commit them as one unit.

```sh
git status          # what changed, what is staged
git diff            # unstaged changes
git diff --staged   # staged changes
git add file.txt    # stage one file
git commit -m "..." # store the staged snapshot
```

## What a repository is

A repository is the `.git/` folder plus your working tree. It contains every commit, branch, and tag for the project. Copying the folder copies the history. Deleting `.git/` deletes the history but leaves the current files.

`git init` starts a repository. It does not contact a server. Everything works offline until you choose to add a remote.

## What a commit contains

A commit records:

- A snapshot of the staged files.
- A message.
- An author and timestamp.
- A pointer to the parent commit.

Git does not store a diff in the commit. It stores the state. Diffs are calculated when you ask for them.

## Ignore what is not source

Some files should not enter history: build output, editor settings, local secrets, large binaries. A `.gitignore` file lists patterns to skip.

```gitignore
node_modules/
dist/
.env
*.log
```

Add `.gitignore` before the first commit when you can. It is easier than removing files from history later.

## Try it

Create a small repository and inspect its states.

1. Run `git init` in a new folder.
2. Create two files: `notes.md` and `draft.md`.
3. Run `git status` and note the untracked files.
4. Stage only `notes.md` and run `git diff --staged`.
5. Commit. Run `git status` again and explain why `draft.md` is still untracked.

Work in `local-project/source/`.

Next: [Commits and history](02-commits-and-history.md)
