# Project Workspace Template

A simple folder structure for learning and running a project. Adopt all of it, part of it, or none of it.

```text
local-project/                  # plain container, not a Git repo
├── pm-vault/                   # team vault, copied from templates/team-vault
├── personal-project-notes/     # personal vault, copied from templates/personal-vault
└── source/                     # Git repo for the project source

backup-remote-location/         # optional local bare remote
└── my-project.git/

hosted-service/                 # GitHub
└── my-project/
```

## Why this shape

- **The container is not a repo.** `local-project/` holds the pieces without creating nested Git repositories.
- **Team visibility is separate from personal notes.** The team vault is shared. The personal vault is private.
- **The vaults are not versioned by default.** Version them only if you want history for your notes.
- **The source is the Git repo.** `source/` is where commits, branches, and merges happen.
- **The backup remote is a practice remote.** It lets you learn push, pull, tags, and pruning without a hosted service.
- **The hosted service is GitHub.** It is a remote service, not a local folder.

## How to set it up

Create the folders you need in your file explorer or terminal:

```text
local-project/
├── pm-vault/
├── personal-project-notes/
└── source/

backup-remote-location/
hosted-service/
```

Copy the entire contents of `templates/team-vault/` into `local-project/pm-vault/`, including the hidden `.obsidian` folder. Copy `templates/personal-vault/` into `local-project/personal-project-notes/` the same way.

Initialize the source repo:

```sh
cd local-project/source
git init
```

Create the bare remote from inside `local-project/source`:

```sh
git init --bare ../../backup-remote-location/my-project.git
```

## Adopt only what you need

| If you only want… | Create |
| --- | --- |
| Project management | `local-project/pm-vault/` |
| Personal execution | `local-project/personal-project-notes/` |
| Git practice | `local-project/source/` |
| Remotes practice | `backup-remote-location/my-project.git` |
| Hosted collaboration | A GitHub repository |

Nothing requires the full structure.

## What goes where

- Project briefs, tasks, decisions, and team notes go in `pm-vault/`.
- Your personal tasks, plans, and reminders go in `personal-project-notes/`.
- Code, scripts, and project files go in `source/`.
- The bare remote mirrors `source/` for practice.
- The GitHub repository is the published version of `source/`.

## Related skills

- [Git](../../guides/git/)
- [Obsidian](../../guides/obsidian/)
- [Project management](../../guides/project-management/)
- [Self-management](../../guides/self-management/)
- [Git services](../../guides/git-services/)

## Related handbook

- [Build your workspace](../../handbook/03-build-your-workspace.md)
- [Adopt in a day](../../handbook/04-adopt-in-a-day.md)
