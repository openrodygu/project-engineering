# Git services

Publish a repository, track work in issues, and review changes through pull requests.

You need a GitHub account. Create one at <https://github.com/join>.

## Do this now

Take 20–30 minutes and publish `local-project/source/` to GitHub, then open an issue and a pull request.

1. **Create the hosted repository.** On GitHub, create a new repository. Keep it empty: no README, no `.gitignore`, no license.

   Then connect your local repository:

   ```sh
   cd local-project/source
   git remote add origin https://github.com/<you>/<repo>.git
   git push -u origin main
   ```

   The published copy represents `hosted-service/`.

2. **Open an issue.** In the repository, create an issue titled `Add project notes`. In the body, write:

   ```markdown
   **Goal:** Add a short notes section to the README.
   **Acceptance criteria:**
   - [ ] README has a Notes section
   - [ ] At least two notes are listed
   ```

3. **Open a pull request.** Create a branch, make the change, push it, and open a pull request that closes the issue:

   ```sh
   git switch -c add-notes
   # edit README.md
   git add README.md
   git commit -m "Add project notes section"
   git push -u origin add-notes
   ```

   On GitHub, open the pull request and write `Closes #1` in the description.

You now have a published repository, a tracked issue, and a reviewable change.

## What it is

A git service adds a shared place for the repository and the work around it:

- **Remote repository** — the shared copy of history.
- **Issues** — a visible backlog of work, bugs, and questions.
- **Pull requests** — a proposal to merge a branch, with discussion and checks.
- **Reviews** — a second pair of eyes before the change lands.
- **Checks** — automated tests and linting on each change.
- **Releases** — tagged versions with notes and assets.

GitHub is the primary service in this guide. GitLab uses different names for the same ideas; see the appendix.

## Go deeper

- [01 Repositories and issues](01-repositories-and-issues.md)
- [02 Pull requests](02-pull-requests.md)
- [03 Code review](03-code-review.md)
- [04 CI and checks](04-ci-and-checks.md)
- [05 Releases and tags](05-releases-and-tags.md)
- [06 Permissions and security](06-permissions-and-security.md)
- [07 GitLab equivalents](07-gitlab-equivalents.md)

Read 01–03 first. Add 04 when you want automation. Read 06 before you invite other people.

## Where this fits

- Hosted repository: `hosted-service/` (GitHub)
- Local source: `local-project/source/`
- Workspace layout: [Project workspace](../../templates/project-workspace/README.md)
- System view: [Handbook](../../handbook/README.md)
- Skill catalog: [Skill catalog](../README.md)

## Common mistakes

- **Creating the GitHub repository with a README when you already have one locally.** The histories diverge on the first push.
- **Opening a pull request with no description.** Reviewers cannot tell what to check.
- **Mixing unrelated changes in one pull request.** The review gets shallow.
- **Leaving issues open after the work ships.** Close them from the pull request with `Closes #N`.
- **Giving everyone admin access.** Use the smallest role that lets people do their job.

## Next skill

[Collaboration](../collaboration/README.md) — write and review changes with other people.
