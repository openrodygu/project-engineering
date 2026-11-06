# Tools and setup

Everything on this page is optional. You do not need any of it to read the handbook or do the exercises in a browser, a notes app, or on paper.

## Read in the browser

You are already doing it. Start at the [README](README.md#start-here) and follow the links. Markdown renders on GitHub. Some links inside `templates/` only work when that folder is open in Obsidian.

## Use the Obsidian templates

The templates are Obsidian vaults (a folder of notes). You need Obsidian on a laptop; you do not need Git.

**Fastest path:** download [team-vault.zip](downloads/team-vault.zip) or [personal-vault.zip](downloads/personal-vault.zip), extract it, and open the inner folder itself (the one containing `_README.md` and `.obsidian`) as a vault in Obsidian.

**From the repo:** download the [handbook ZIP](https://github.com/openrodygu/project-engineering/archive/refs/heads/main.zip) or `git clone https://github.com/openrodygu/project-engineering.git`, extract it, and copy `templates/team-vault/` or `templates/personal-vault/` to a folder you can find. If your file manager hides dot-folders, turn on hidden files so `.obsidian` comes along. On Windows they are visible by default; on macOS press `Cmd+Shift+.`, on Linux press `Ctrl+H`.

In Obsidian, choose **Open folder as vault** and select the folder.

If you used the ready-to-open ZIP, your vault folder is named `team-vault` or `personal-vault`. The `local-project/pm-vault` paths in the guides apply only to the workspace copy.

Each vault includes one community plugin: dotpm in the team vault, TaskNotes in the personal vault. The notes are Markdown; the plugin is compiled code and can read and write files in the vault. Obsidian asks you to trust the vault so the plugin can run. If you would rather install it yourself, see [templates/README.md](templates/README.md). Both paths run third-party plugin code.

New to Obsidian? [Obsidian basics](guides/obsidian/00-obsidian-basics.md) covers install, the interface, links, properties, and Markdown.

## Use Git and Git services

- [Git](guides/git/README.md) — create a local repository and learn commits, branches, and remotes.
- [Git services](guides/git-services/README.md) — publish a repository, open an issue, and review a pull request.

## Build a workspace

The [project workspace template](templates/project-workspace/README.md) shows a simple structure:

```text
local-project/                  # plain container, not a Git repo
├── pm-vault/
├── personal-project-notes/
└── source/

backup-remote-location/         # optional local bare remote
└── my-project.git/

hosted-service/                 # GitHub, not a local folder
└── my-project/
```

The vaults are not versioned by default. The `source/` folder is the Git repository. The rest is optional.

## Where to go next

- [Downloads README](downloads/README.md) — what is in each ZIP.
- [Templates README](templates/README.md) — screenshots, setup, and zero-trust options.
- [Obsidian basics](guides/obsidian/00-obsidian-basics.md) — install, the interface, links, properties, and Markdown.
- [README](README.md) — start the handbook.
