# CI and checks

Let a machine run the boring checks on every change, so review can focus on judgment.

## What CI is

Continuous integration (CI) runs automated steps when code changes: install dependencies, run tests, lint, build, and sometimes deploy a preview. The result appears on the pull request as a check.

The point is fast feedback. A broken change should fail before a person spends time reviewing it.

## A first workflow

GitHub Actions reads workflow files from `.github/workflows/`. Start small:

```yaml
name: checks

on:
  pull_request:
  push:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
      - run: npm ci
      - run: npm test
      - run: npm run lint
```

Adjust the commands to your project. If you do not have tests yet, start with a build or a syntax check. A check that never fails is not useful, but a check that catches one real break is.

## Read the check

On a pull request, the checks appear near the merge button. A red check means something failed. Open the log and find the first real error, not the last line.

Common failures:

- A dependency is missing from the lockfile.
- The test passes locally but needs a service that CI does not have.
- The lint rule is stricter in CI than in the editor.
- A secret is missing from the CI environment.

Fix the cause, push again, and watch the new run.

## Required checks

Repositories can require certain checks before a pull request can merge. Use this for checks the team actually trusts:

- Tests.
- Lint.
- Build.
- Security scan.

Do not require a check that is flaky. A check people routinely ignore trains them to ignore all checks.

## Secrets and safety

- Store tokens in the repository's secrets settings, never in the workflow file.
- Give CI tokens the smallest scope that works.
- Do not print secrets in logs.
- Be careful with workflows from forks; they may run untrusted code.
- Pin third-party actions to a version you trust.

## Keep it fast

A slow pipeline gets bypassed. Aim for a few minutes on a pull request.

- Cache dependencies.
- Run the fastest checks first.
- Split long test suites.
- Do not rebuild everything when one file changed.

## Try it

Add one check to your repository.

1. Create `.github/workflows/checks.yml` with a build or test step.
2. Push it on a branch and open a pull request.
3. Watch the check run.
4. Break something on purpose, push, and confirm the check fails.
5. Fix it and confirm the check passes.

Do this on GitHub. In the workspace map, this is the `hosted-service/` part.

Next: [Releases and tags](05-releases-and-tags.md)
