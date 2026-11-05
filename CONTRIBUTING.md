# Contributing

You can use this repo locally or contribute improvements. Both are welcome.

## Ways to use the repo

### Learn locally

- Clone the repo.
- Do the skill quick starts in your own practice folders.
- No fork or PR is required to learn.
- Keep your work local, or version it in your own repository.

### Contribute

- Fork the repo.
- Create a branch: `skill/<name>`, `fix/<scope>`, or `docs/<scope>`.
- Make one focused change.
- Open a pull request using the template.

## What to contribute

- A new skill or chapter.
- A clearer quick start.
- A concrete example or artifact.
- A fix for a broken link, unclear instruction, or outdated tool detail.
- A bug report or skill request.

## Skill page format

Each skill has a `README.md` and numbered chapters.

The `README.md` starts with:

1. **Do this now** — a 15–30 minute exercise with a concrete artifact.
2. **What it is** — the minimum mental model.
3. **Go deeper** — links to the chapters.
4. **Where this fits** — how it connects to the workspace and templates.
5. **Common mistakes**.
6. **Next skill** — optional.

Keep the quick start first. Depth comes later.

## Style

- Use plain language.
- Prefer concrete examples over abstractions.
- Use “adopt” for taking a practice or template into your own context.
- Use “practice” for exercises.
- Use “apply” for using something on a real project.
- Avoid “implement,” “impose,” “mandate,” and “enforce.”
- Keep headings short.
- Use standard Markdown links so GitHub renders them.
- Use Obsidian wikilinks only inside the vault templates.

## Local-first rule

Do not make a skill depend on the workspace template or on other skills.

If a skill mentions the workspace, say something like:

> If you are not using the workspace template, use any folder you like.

## Before opening a PR

- Check that relative links resolve.
- Check that no secrets, tokens, or internal data were added.
- Check that the quick start still produces an artifact.
- Check that the skill still works without the other skills.
- Confirm no `workspace.json` files were added.
- If you update a plugin in a template, update `templates/README.md` and `CREDITS.md`.

## Commit messages

Use the repo’s commit style:

```text
[type](scope): subject
```

Examples:

```text
[docs](git): clarify remote setup
[fix](obsidian): correct template link
[feat](handbook): add adoption roadmap
```

## License

By contributing, you agree that your contributions are licensed under the repository’s MIT license.
