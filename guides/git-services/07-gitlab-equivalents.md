# GitLab equivalents

A short translation table. The ideas are the same; the names and menus differ.

## Names

| GitHub | GitLab |
| --- | --- |
| Repository | Project |
| Organization | Group |
| Issue | Issue |
| Pull request | Merge request |
| Review approval | Approval |
| GitHub Actions | GitLab CI/CD |
| Workflow file | `.gitlab-ci.yml` |
| Release | Release |
| Branch protection | Protected branches |
| CODEOWNERS | Code owners |
| Dependabot | Dependency scanning |
| Secret scanning | Secret detection |
| Gist | Snippet |

## What changes in practice

- **Merge requests** replace pull requests. The flow is the same: branch, push, open, review, merge.
- **Pipelines** replace workflows. A `.gitlab-ci.yml` file defines stages and jobs.
- **Protected branches** control who can push and merge to `main`.
- **Approvals** can require one or more approvers before a merge.
- **Groups** hold projects and manage access at a higher level.
- **Releases** attach notes and assets to a tag, much like GitHub releases.

## A minimal pipeline

```yaml
stages:
  - test

test:
  stage: test
  image: node:20
  script:
    - npm ci
    - npm test
```

The structure is shorter than a GitHub Actions workflow, but the purpose is the same: run checks on every change.

## What stays the same

- Commit early and often.
- Use short branches.
- Keep merge requests small.
- Write a description with what, why, and how to check.
- Review for correctness, clarity, and risk.
- Tag releases and write notes.
- Limit access and protect the main branch.

If you move between services, the habits transfer. Only the buttons move.

## Try it

Map one workflow to GitLab terms.

1. Write down your current branch and merge process.
2. Rewrite each step using GitLab names: project, merge request, pipeline, protected branch.
3. Identify one step that has no direct equivalent and decide how you would handle it.

This appendix is optional. Do this only if your team uses GitLab or you expect to.

Next: [Collaboration](../collaboration/README.md) — work with other people on changes.
