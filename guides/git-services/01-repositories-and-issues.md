# Repositories and issues

Create a shared home for the code and turn work into Issues people can see and close.

## Create the repository

On GitHub:

1. Choose **New repository**.
2. Pick a clear name and a short description.
3. Choose visibility: private by default, public when the work is meant to be open.
4. Do not add a README, license, or `.gitignore` if you already have them locally.
5. Create the repository, then push your local `main`.

```sh
git remote add origin https://github.com/<you>/<repo>.git
git push -u origin main
```

A hosted README is the front door. Add one that says what the project is, how to run it, and where to ask questions.

## What an issue is

An issue is a tracked unit of work. It can be a bug, a task, a question, or a proposal. It lives in the open, so the team can see what is planned and what is blocked.

A useful issue has:

- A specific title.
- The problem or goal.
- Acceptance criteria.
- A label, an assignee, and a milestone when they help.
- Links to related issues or decisions.

```markdown
**Problem:** New team members cannot tell which branch is safe to deploy.

**Goal:** Document the branch model in the README.

**Acceptance criteria:**
- [ ] README explains main, feature, and release branches
- [ ] One diagram shows the flow
- [ ] A new contributor can follow it without asking
```

## Labels and milestones

Labels group work by type or area: `bug`, `docs`, `infra`, `question`. Keep the list short. A label nobody uses is noise.

Milestones group work by target: `v0.2`, `Q2 hardening`, `Launch`. Use a milestone when the date or scope matters. Do not create one for every week.

## Templates

A repository can hold issue templates so reports arrive with the right detail. Add them under `.github/ISSUE_TEMPLATE/`.

A bug template usually asks for:

- What happened.
- What you expected.
- Steps to reproduce.
- Version and environment.
- Logs or screenshots.

A task template asks for the goal, acceptance criteria, and links. Templates reduce back-and-forth; they do not replace judgment.

## Keep the list honest

- Close issues when the work ships, not when someone remembers.
- Link pull requests to issues with `Closes #12`.
- Split large issues into smaller ones before work starts.
- Use one issue per outcome. "Improve everything" is not closable.

## Try it

Create one issue that someone else could pick up.

1. Write a specific title.
2. Add the goal and three acceptance criteria.
3. Add one label and one assignee.
4. Link it to a project note or a decision record if one exists.

Do this on GitHub. In the workspace map, this is the `hosted-service/` part.

Next: [Pull requests](02-pull-requests.md)
