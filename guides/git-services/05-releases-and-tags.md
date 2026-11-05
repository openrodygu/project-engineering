# Releases and tags

Mark what shipped, write down what changed, and make the version easy to find later.

## Version numbers

Use semantic versioning for most software:

- **MAJOR** — a breaking change.
- **MINOR** — a new feature that stays compatible.
- **PATCH** — a fix that stays compatible.

`1.4.2` means major 1, minor 4, patch 2. Start at `0.1.0` while the interface is still moving. Use `1.0.0` when you are ready to keep compatibility promises.

## Tags

A tag marks a specific commit. Use an annotated tag for a release so it carries a message and a date.

```sh
git tag -a v1.4.2 -m "Fix login timeout"
git push origin v1.4.2
```

List tags with:

```sh
git tag --list
git show v1.4.2
```

Tags are not branches. They do not move when new commits arrive. That is the point: a tag identifies exactly what shipped.

## Create a release

On GitHub, a release wraps a tag with notes and optional files.

1. Open **Releases** and choose **Draft a new release**.
2. Pick an existing tag or create a new one.
3. Write a title and release notes.
4. Attach build artifacts if people need them.
5. Mark it as a pre-release if it is not ready for general use.
6. Publish.

A release page is what most people will read. Write it for them, not for the commit log.

## Release notes

Group changes by what they mean to the reader:

```markdown
## Added
- Vendor comparison export

## Fixed
- Login no longer hangs on slow networks

## Changed
- Default timeout is now 10 seconds

## Upgrade notes
- Re-run the migration before starting the service
```

Link issues and pull requests. Mention breaking changes first.

## A simple release checklist

- [ ] All intended changes are merged.
- [ ] Checks pass on the release commit.
- [ ] Version number follows the change type.
- [ ] Tag is annotated and pushed.
- [ ] Release notes are written.
- [ ] Upgrade steps are included if needed.
- [ ] The team knows what shipped.

## Try it

Publish one release.

1. Tag your current commit `v0.1.0` with an annotated tag.
2. Push the tag.
3. Create a GitHub release from that tag.
4. Write three sections: Added, Fixed, and Upgrade notes.
5. Confirm the tag and release point to the same commit.

Do this on GitHub. In the workspace map, this is the `hosted-service/` part.

Next: [Permissions and security](06-permissions-and-security.md)
