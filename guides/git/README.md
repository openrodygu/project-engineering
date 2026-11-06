# Git

Track changes, experiment safely, and keep a history you can trust.

You need Git installed. Check with `git --version`. If it is missing, install it from <https://git-scm.com/downloads>.

## Do this now

Take 20–30 minutes and build a small repository with a real branch and merge. Use `local-project/source/`.

Create the folder `local-project/source` in your file explorer or terminal, open a terminal in it, and initialize the repository:

```sh
git init
```

If this is your first time using Git, set your identity once:

```sh
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Create a file named `README.md` with your editor and add a title and one sentence. Then make the first commit:

```sh
git add README.md
git commit -m "Add project README"
git branch -M main
```

Create a branch, add a short notes section to `README.md` with your editor, and merge it back:

```sh
git switch -c add-notes
git add README.md
git commit -m "Add project notes"
git switch main
git merge add-notes
```

Check the result:

```sh
git log --oneline --graph --all
git branch
```

You now have a repository with a main line, a branch, and a merge. That is the core loop you will use every day.

## What it is

Git stores snapshots of your project. Each commit is a snapshot plus a message and a pointer to its parent. Branches are movable labels on those commits. A merge joins two lines of history.

The working area has three states:

- **Working tree** — the files you see and edit.
- **Staging area** — the changes you selected for the next commit.
- **Repository** — the commits Git has stored.

You edit in the working tree, stage what belongs together, and commit a coherent change. A remote is just another copy of the repository that you can push to and pull from.

## Go deeper

- [01 Version control](01-version-control.md)
- [02 Commits and history](02-commits-and-history.md)
- [03 Branches and merges](03-branches-and-merges.md)
- [04 Conflicts](04-conflicts.md)
- [05 Remotes and backup](05-remotes-and-backup.md)
- [06 Workflows](06-workflows.md)
- [07 Undoing and hygiene](07-undoing-and-hygiene.md)

Read 01–03 first. Read 05 before you rely on a remote. Read 07 before you need it in a hurry.

## Where this fits

- Git repository: `local-project/source/`
- Optional workspace: [Project workspace](../../templates/project-workspace/README.md)
- System view: [Handbook](../../handbook/README.md)
- Skill catalog: [Skill catalog](../README.md)

## Common mistakes

- **Committing everything at once.** One huge commit hides what changed and why.
- **Writing commit messages like "fix" or "update".** Future you will not know what was fixed.
- **Working directly on main for every change.** Branches are cheap; use them for experiments.
- **Pulling without checking what changed.** Read the diff before you merge a stranger's work.
- **Treating a local commit as a backup.** A commit on one disk is not a backup. Push or copy it.

## Next skill

[Git services](../git-services/README.md) — publish the repository, open an issue, and review a pull request.
