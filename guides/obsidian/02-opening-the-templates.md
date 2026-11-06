# Opening the templates

The templates are ready to use. Open them once and inspect what is already configured. That is faster than installing plugins from scratch.

## Copy the vaults

Create `local-project/pm-vault` and `local-project/personal-project-notes` in your file explorer or terminal.

Copy the entire contents of `templates/team-vault/` into `pm-vault/`, and the entire contents of `templates/personal-vault/` into `personal-project-notes/`.

Make sure the `.obsidian` folder comes along. It carries the plugins and settings. On Windows, dot-folders are visible by default. On macOS, press `Cmd+Shift+.`; on Linux, press `Ctrl+H`.

## Open them as vaults

1. Launch Obsidian.
2. Choose **Open folder as vault**.
3. Select `local-project/pm-vault/`.
4. When Obsidian asks whether you trust the author, choose **Trust author and enable plugins**.
5. Repeat for `local-project/personal-project-notes/`.

Do not open a single note. Open the folder.

## Check the team vault

1. Open `_README.md` and read the two-vault section.
2. Open the **Project manager** pane from the left ribbon.
3. Open **Example Project**.
4. Look at the table. You should see tasks such as "Define scope" and "Research options".
5. Open one task and read its properties, description, assignee, and status.

dotpm is the first team project management tool in this workspace. The project list, table, Gantt, and board all come from it.

## Check the personal vault

1. Open `_README.md`.
2. Open `TaskNotes/Start Here.md`.
3. Work through the tour in place.
4. Create one task from the command palette when the tour asks you to.

TaskNotes is the first personal project management tool in this workspace. It stores one note per task in `TaskNotes/Tasks` and uses Bases for its views.

## If something is missing

| Symptom | Check |
| --- | --- |
| No **Project manager** pane | Community plugins are enabled for the team vault |
| No TaskNotes views | **Bases** is enabled under Core plugins, and TaskNotes under Community plugins |
| Notes open but links are dead | You opened a file, not the vault folder |
| Settings look empty | The `.obsidian` folder did not copy |

## Try it

Confirm that `.obsidian/plugins/` exists in both copies. Then open **Example Project** in the team vault and `TaskNotes/Start Here.md` in the personal vault. Do not change any settings yet.

Next: [03 Markdown and notes](03-markdown-and-notes.md)
