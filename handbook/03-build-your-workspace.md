# Build your workspace

The skills are easier when they share one workspace. You can use the structure below, change it, or ignore it.

## The structure

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

- **`local-project/` is a container.** It keeps the pieces together without becoming a nested Git repo.
- **The vaults are separate from the source.** Team visibility and personal notes are not the same as code history.
- **The vaults are not versioned by default.** Versioning them is optional and up to you.
- **`source/` is the Git repo.** That is where commits, branches, and merges happen.
- **`backup-remote-location/` is a practice remote.** It lets you learn push, pull, tags, and pruning without a hosted service.
- **`hosted-service/` is GitHub.** It is a remote service, not a local folder.

## How to set it up

Create the folders in your file explorer or terminal:

```text
local-project/
├── pm-vault/
├── personal-project-notes/
└── source/

backup-remote-location/
hosted-service/
```

Copy the contents of `templates/team-vault/` into `local-project/pm-vault/`, including the hidden `.obsidian` folder. Do the same with `templates/personal-vault/` and `local-project/personal-project-notes/`.

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

## Try it

Create the folders you need.

Then write one sentence in a note:

> This workspace exists so that ______ is visible, ______ is private, and ______ is versioned.

Next: [Adopt in a day](04-adopt-in-a-day.md)
