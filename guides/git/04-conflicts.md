# Conflicts

Resolve overlapping changes calmly by understanding both sides before choosing.

## Why conflicts happen

A conflict occurs when two branches change the same lines, or one branch edits a file another branch deletes. Git cannot know which version is correct, so it stops and asks you.

A conflict is not an error. It is Git refusing to guess.

## Read the markers

When a conflict happens, the file contains markers:

```text
<<<<<<< HEAD
The current branch version.
=======
The incoming branch version.
>>>>>>> add-notes
```

- `HEAD` is the branch you are merging into.
- The other label is the branch being merged.
- Your job is to produce the final text and remove all three markers.

## Resolve step by step

1. Run `git status` to see which files conflict.
2. Open each file and read both sides.
3. Decide the final content. Keep one side, combine them, or write something new.
4. Remove the markers.
5. Run the tests or check the result.
6. Stage the resolved file with `git add`.
7. Commit the merge.

```sh
git status
# edit the files
git add resolved-file.md
git commit
```

If you get lost, abort and start again:

```sh
git merge --abort
```

Aborting is safe before you commit the merge.

## Prefer understanding over speed

Do not pick "ours" or "theirs" for every file just to finish. That is how one team's work disappears. Read the intent of both changes.

Ask:

- What was the other branch trying to do?
- Is this a real disagreement or just adjacent edits?
- Does the combined result still make sense?

When the intent is unclear, ask the author. A two-minute question beats a silent regression.

## Reduce future conflicts

- Keep branches short-lived.
- Pull main into your branch regularly.
- Keep commits small and focused.
- Avoid reformatting whole files in a feature branch.
- Do not edit the same large file from two long branches if you can split it.

## Try it

Create a conflict on purpose and resolve it.

1. On `main`, change line 1 of a file and commit.
2. Create a branch from the previous commit and change the same line differently. Commit.
3. Merge the branch into `main`.
4. Read the markers, choose a combined result, remove the markers, and commit.
5. Run `git log --oneline --graph` and confirm the merge.

Work in `local-project/source/`.

Next: [Remotes and backup](05-remotes-and-backup.md)
