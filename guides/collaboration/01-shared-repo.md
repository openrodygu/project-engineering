# Shared repo

A shared repository is a place where more than one person can propose, discuss, and land changes without overwriting each other. Git provides the history. A hosting service provides the place to talk about it.

## The moving parts

- **The default branch** is the current agreed version. It should stay usable.
- **Branches** let you work without disturbing others.
- **Issues** describe work and decisions.
- **Pull requests** propose a branch for review and merging.
- **Reviews** check the proposal before it lands.
- **Commit history** records what changed and why.

The hosted-repo mechanics — creating a repository, opening a pull request, requesting a review — are covered in [Git services](../git-services/). This skill focuses on how to use them well.

## Who does what

| Role | Responsibility |
| --- | --- |
| **Author** | Describes the change, keeps it small, responds to review |
| **Reviewer** | Checks correctness, risk, tests, and clarity |
| **Maintainer** | Keeps the branch healthy and makes the merge call |

One person can hold more than one role. The point is that each role has a job, not a title.

## What good looks like

- The issue says what problem is being solved.
- The branch has one purpose.
- The PR description lets a reviewer start without asking basic questions.
- The review comments are specific and kind.
- The decision is written down where the next person can find it.

## What to agree on early

Before the first PR, agree on a small set of conventions:

- What the default branch is called.
- How to run tests.
- Who reviews what.
- What must be in a PR description.
- Where decisions are recorded.

Write these in the repository README or a short `CONTRIBUTING.md`. A convention nobody can find is not a convention.

## Try it

Open a repository you use and write down:

1. The default branch name.
2. The command or steps to run its tests.
3. The person or group that reviews changes.
4. Where a decision would be written down.

If you cannot answer one of these, that is the first thing to fix.

Next: [02 Issues and task breakdown](02-issues-and-task-breakdown.md)
