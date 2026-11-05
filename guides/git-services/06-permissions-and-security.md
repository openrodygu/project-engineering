# Permissions and security

Give people the access they need, protect the main line, and keep secrets out of the repository.

## Roles

Hosted services use roles with different powers. A common set:

| Role | Can do | Use for |
| --- | --- | --- |
| Read | View and clone | Stakeholders, observers |
| Triage | Manage issues and pull requests | Team leads, maintainers |
| Write | Push branches and merge | Contributors |
| Maintain | Manage settings without full control | Senior maintainers |
| Admin | Change everything, including access | One or two people |

Start with the smallest role. Add more when the person has a real need. Admin access is not a status symbol; it is a risk.

## Protect the main line

Branch protection keeps mistakes and accidents away from the branch people deploy.

Common settings:

- Require a pull request before merging.
- Require one approval.
- Require checks to pass.
- Require the branch to be up to date.
- Block force pushes.
- Restrict who can push directly.

Use the lightest set that matches your risk. A solo repository may need only "no force push". A production repository needs more.

## Secrets

Never commit secrets, tokens, passwords, or private keys. Put them in the service's secrets settings or a local environment file that is ignored.

If a secret is committed:

1. Treat it as leaked.
2. Rotate or revoke it first.
3. Remove it from the working tree.
4. Rewrite history only if the repository is private and you understand the impact.
5. Tell the people who need to know.

Deleting the file in a new commit does not remove it from history. Rotation is the part that protects you.

## Access review

Once a quarter, or when someone leaves:

- List collaborators and their roles.
- Remove people who no longer need access.
- Check deploy keys, personal tokens, and integrations.
- Review outside collaborators.
- Confirm the owner list is current.

An access list nobody reviews becomes a list of former contributors with keys.

## Useful defaults

- Turn on two-factor authentication for the organization.
- Turn on Dependabot alerts and security updates for dependencies.
- Turn on secret scanning where the plan provides it.
- Use signed commits for release tags if your team values provenance.
- Keep the repository private until there is a reason to publish.

## Try it

Audit one repository.

1. List every collaborator and their role.
2. Remove or downgrade one person who does not need the access.
3. Confirm the main branch requires a pull request and a passing check.
4. Turn on dependency alerts or secret scanning if available.
5. Write one sentence on what you changed and why.

Do this on GitHub. In the workspace map, this is the `hosted-service/` part.

Next: [GitLab equivalents](07-gitlab-equivalents.md)
