# Remotes and backup

Copy history to another location, keep it current, and know what is local versus shared.

## What a remote is

A remote is a named URL for another copy of the repository. `origin` is the default name for the copy you cloned from or pushed to first.

```sh
git remote -v
git remote add origin <url>
```

A remote can be a hosted service such as GitHub, or a bare repository on a disk or server. Git treats both the same way.

## Push, pull, fetch

- **Push** sends your commits to the remote.
- **Fetch** downloads new commits but does not change your working tree.
- **Pull** fetches and then integrates the changes into your branch.

```sh
git push -u origin main
git fetch origin
git pull
```

`-u` sets the upstream branch so later pushes and pulls need no arguments.

Use `fetch` when you want to inspect before merging. Use `pull` when you trust the branch and want it current.

## Tracking branches

A local branch can track a remote branch. That link tells Git where to push and what to compare against.

```sh
git branch -vv
git status
```

`git status` reports whether you are ahead, behind, or diverged. Read it before pushing.

## Tags

Tags mark a specific commit, usually a release.

```sh
git tag -a v0.1.0 -m "First release"
git push origin v0.1.0
git push origin --tags
```

Annotated tags carry a message and date. Lightweight tags are just pointers. Use annotated tags for releases.

## Prune stale references

When branches are deleted on the remote, your local list may still show them.

```sh
git fetch --prune
git branch -vv        # gone branches are marked
git branch -d old-branch
```

Pruning only removes remote-tracking references. It does not delete your local branches.

## Bare remotes for backup

A bare repository has no working tree. It is a clean copy of history that you can use as a local backup or practice remote.

```sh
git init --bare ../../backup-remote-location/my-project.git
git remote add backup ../../backup-remote-location/my-project.git
git push -u backup main
```

This gives you a second copy on another disk or folder. It is not a substitute for an off-site backup, but it is much better than one copy on one laptop.

## A simple backup rule

1. Commit your work.
2. Push to at least one remote you do not control alone.
3. Check that the push succeeded.
4. Test a clone now and then. A backup you have never restored is a hope.

## Try it

Create a bare remote and use it.

1. From `local-project/source`, create `../../backup-remote-location/my-project.git` with `git init --bare`.
2. Add it as a remote called `backup`.
3. Push `main` and a tag.
4. Clone the bare repository into a temporary folder and confirm the files and history exist.
5. Create a temporary branch, push it to `backup`, delete it with `git push backup --delete <branch>`, then run `git fetch --prune` and watch the stale remote reference disappear.

Work from `local-project/source/`.

Next: [Workflows](06-workflows.md)
