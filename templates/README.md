# Templates

Working templates for the skills in this repo. Each is optional.

- **[team-vault](team-vault/)** — shared team visibility using **dotpm**.
- **[personal-vault](personal-vault/)** — private task tracking using **TaskNotes**.
- **[project-workspace](project-workspace/README.md)** — the folder structure around them.

The team vault answers *what is the team doing and where does it stand?* The personal vault answers *what am I doing today?*

All templates are sanitized. They contain a generic `Example Project`, placeholder people, and no real project data.

---

## Quick start

To read the handbook itself in Obsidian, open the repo root folder as a vault. The vault templates below are separate vaults. New to Obsidian? See [Obsidian basics](../guides/obsidian/00-obsidian-basics.md).

Templates require Obsidian. The handbook itself does not.

| Team vault (dotpm) | Personal vault (TaskNotes) |
| --- | --- |
| <img src="../assets/dotpm-dashboard.png" alt="dotpm team dashboard" width="420"> | <img src="../assets/tasknotes-demo.gif" alt="TaskNotes personal task views" width="420"> |

These are the plugins’ own demo screenshots, not this repo’s Example Project. Both projects are MIT licensed.

### 1. Get a vault

**Fastest path:** download [team-vault.zip](../downloads/team-vault.zip) or [personal-vault.zip](../downloads/personal-vault.zip), extract it, and open the inner folder itself (the one containing `_README.md` and `.obsidian`) as a vault in Obsidian. The ZIP includes the plugin setup.

**From the repo:** [download the handbook ZIP](https://github.com/openrodygu/project-engineering/archive/refs/heads/main.zip), extract it, and copy `templates/team-vault/` or `templates/personal-vault/` into a workspace folder. Copy the whole folder, including the `.obsidian` directory.

```text
local-project/
├── pm-vault/                   # copy of team-vault
└── personal-project-notes/     # copy of personal-vault
```

If your file manager hides dot-folders, turn on hidden files before copying. On Windows they are visible by default. On macOS, press `Cmd+Shift+.` in Finder; on Linux, press `Ctrl+H`.

### 2. Open and trust the vault

In Obsidian, choose **Open folder as vault** and select the folder.

Each vault includes one community plugin: dotpm in the team vault, TaskNotes in the personal vault. Obsidian asks you to trust the vault so that plugin can run. The notes are plain Markdown; the plugin is compiled JavaScript and its settings live in `.obsidian/`. You can inspect the files before you open the vault. The plugins are MIT licensed; see [CREDITS.md](../CREDITS.md).

**Zero-trust option (install the plugins yourself).** This avoids running the copies bundled in this repo, but you still trust the plugin developers when you install from the store.

1. Extract the ZIP or copy the folder.
2. Delete `.obsidian/plugins/`. This also removes the template's plugin settings (`data.json`), so statuses, priorities, folders, and views need to be set up again.
3. Open the folder as a vault. Keep Restricted mode on if you do not want any community plugins to run.
4. To install from the store, turn off Restricted mode, open **Settings → Community plugins → Browse**, and search for **Project Manager** (the plugin's internal name is dotpm) or **TaskNotes**.
5. Reconfigure the plugin settings, or copy the settings from the template if you trust them.

The Markdown guides still work without the plugins. You lose the preconfigured board and task views.

### 3. Open the README

- Team vault: open `_README.md`, then open **Example Project**.
- Personal vault: open `_README.md`, then work through `TaskNotes/Start Here.md`.

### 4. Adopt what fits

Change the project name, people, statuses, and tasks. Keep what helps. Remove what does not.

---

## Team vault

- dotpm is included and enabled.
- The project list opens from the **Project manager** pane.
- `Example Project` shows the project and task structure.
- The vault includes team-facing guides for Obsidian, dotpm, TaskNotes, and project management.

## Personal vault

- TaskNotes is included and enabled.
- Bases is enabled for the TaskNotes views.
- `TaskNotes/Start Here.md` is a guided tour.
- The vault includes personal guides for Obsidian, TaskNotes, shared-vault boundaries, and self-management.

## Project workspace

The workspace template is a README only. It shows a structure and explains why and how to adopt it. See [project-workspace/README.md](project-workspace/README.md).

---

## Requirements

- Obsidian **1.13 or newer** (dotpm requires 1.13; TaskNotes requires 1.12.2+).
- Desktop for setup. Template setup copies a hidden `.obsidian` folder; use a desktop file manager. Mobile can open a vault after it is set up.
- No account is required to read the handbook or use the templates. Optional calendar and API integrations are off by default.

---

## What is included

Each vault template includes:

- The Markdown guides.
- A small example project or task setup.
- Obsidian core plugin configuration.
- The required community plugin binaries and settings.
- The Border theme and theme configuration.

Each vault template excludes:

- `workspace.json`, so Obsidian creates a fresh layout for each user.
- Personal notes, real project data, and local paths.
- Any API tokens or credentials.

The vaults are not versioned by default. Versioning them is optional and up to you.

---

## Tested versions

| Component | Version |
| --- | --- |
| dotpm | 2.6.0 |
| TaskNotes | 4.16.1 |
| Border theme | 1.13.9 |

Newer plugin versions should work. If you update a plugin, let Obsidian manage the plugin folder.

---

## Customize

- Replace **Example Project** with your project name.
- Replace **Alice**, **Bob**, **Carol**, and **Dave** with your team.
- Update the project description, tasks, and dates.
- Adjust statuses and priorities in the plugin settings if needed.
- Keep the two-vault boundary: team commitments in the shared vault, personal execution in the personal vault.

See `team-vault/_README.md` and `personal-vault/_README.md` for the workflow rules.

---

## Attribution

This repo includes third-party Obsidian plugins and a theme. See [CREDITS.md](../CREDITS.md) for authors, versions, and links.

- dotpm — MIT licensed.
- TaskNotes — MIT licensed.
- Border theme — third-party theme by Akifyss; see the upstream repository for its license.

Obsidian itself is not included.

---

## License

The guides and templates in this repository are MIT licensed. See [LICENSE](../LICENSE).
