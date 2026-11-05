# Pull requests

Propose a change, explain why it matters, and give reviewers what they need to say yes.

## The flow

1. Start from an up-to-date `main`.
2. Create a branch with a clear name.
3. Make small commits.
4. Push the branch.
5. Open a pull request.
6. Respond to review, then merge.

```sh
git switch main
git pull
git switch -c fix-login-timeout
# edit, add, commit
git push -u origin fix-login-timeout
```

On GitHub, open the pull request from the branch and choose the target branch.

## Write a useful description

A pull request description answers three questions:

- What changed?
- Why?
- How did you check it?

```markdown
## What
Add a timeout to the login request.

## Why
Slow networks caused the form to hang indefinitely.
Closes #18.

## How to check
1. Throttle the network in dev tools.
2. Submit the login form.
3. Confirm the error appears after 10 seconds.
```

Link the issue with `Closes #18` so it closes when the pull request merges. Add screenshots or logs when the change is visual or the failure is hard to reproduce.

## Keep it small

A reviewer can hold one logical change in their head. They cannot hold a refactor, a feature, and a formatting sweep at once.

- One change per pull request.
- Separate refactoring from behavior.
- Separate formatting from logic.
- Split a large feature into a sequence of reviewable steps.
- Keep the branch short-lived.

Small pull requests are reviewed faster and reverted more safely.

## Draft and ready

Open a draft pull request when you want early feedback or want to show the direction. Mark it ready when it is complete and tested. A draft tells reviewers not to spend time on a final review yet.

## Merge strategies

- **Merge commit** — keeps the branch history and adds a merge commit. Good for feature branches.
- **Squash and merge** — combines the branch into one commit. Good for noisy work-in-progress history.
- **Rebase and merge** — replays the commits on main for a linear history. Good for small, clean branches.

Pick one default for the repository and use it consistently. The team should not debate the button on every pull request.

## After the merge

- Delete the branch, locally and on the remote.
- Pull `main` so your next branch starts current.
- Confirm the linked issue closed.
- If the change needs a release, tag it.

## Try it

Open a pull request for your repository.

1. Create a branch called `add-notes`.
2. Make one small commit.
3. Push the branch and open a pull request.
4. Write the What, Why, and How to check sections.
5. Link an issue with `Closes #N`.

Do this on GitHub. In the workspace map, this is the `hosted-service/` part.

Next: [Code review](03-code-review.md)
