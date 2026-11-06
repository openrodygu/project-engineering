# Obsidian

Obsidian turns a folder of Markdown files into a workspace for notes, team projects, and personal tasks.

You need Obsidian installed. Download it from <https://obsidian.md>.

New to Obsidian? Read [00 Obsidian basics](00-obsidian-basics.md) first. It covers install, opening a vault, links, properties, and Markdown.

## Do this now

15–30 minutes. You will finish with two open vaults, one team task, and one personal task.

1. Copy `templates/team-vault/` into `local-project/pm-vault/`.
2. Copy `templates/personal-vault/` into `local-project/personal-project-notes/`.
3. In Obsidian, choose **Open folder as vault** and open `local-project/pm-vault/`.
4. Open `local-project/personal-project-notes/` as a second vault.
5. Trust the author and enable community plugins in both vaults.
6. In the team vault, open the **Project manager** pane and open **Example Project**.
7. In the personal vault, open `TaskNotes/Start Here.md` and work through it.
8. Create one task in **Example Project** with a verb-first title, an assignee, and a due date.
9. Create one personal task with a context and a 30-minute estimate.

The team vault uses **dotpm** as the first team project management tool. It answers *what is the team doing and where does it stand?* The personal vault uses **TaskNotes** as the first personal project management tool. It answers *what am I doing today?*

## What it is

Obsidian is a Markdown editor that treats a folder on your computer as a **vault**. Every note is a `.md` file, and folders are real folders. Two ideas make it more than a text editor:

- **Links** connect notes and show backlinks.
- **Properties** store structured `key: value` data at the top of a note.

The workspace separates work into two vaults. The team vault uses dotpm for shared projects, tasks, dependencies, and status. The personal vault uses TaskNotes for your own tasks, contexts, estimates, and daily plan. Nothing syncs between them. When personal work becomes team work, you promote it by hand.

You learn Obsidian faster by opening the templates and doing one real task in each than by reading about plugins in the abstract.

## Go deeper

0. [Obsidian basics](00-obsidian-basics.md)
1. [01 Vaults and the two-vault model](01-vaults-and-the-two-vault-model.md)
2. [02 Opening the templates](02-opening-the-templates.md)
3. [03 Markdown and notes](03-markdown-and-notes.md)
4. [04 Links, properties, and dotpm](04-links-properties-and-dotpm.md)
5. [05 Bases and TaskNotes](05-bases-and-tasknotes.md)
6. [06 Plugins and themes](06-plugins-and-themes.md)
7. [07 Sync and backup](07-sync-and-backup.md)
8. [08 Sharing and publishing](08-sharing-and-publishing.md)

## Where this fits

- Team vault: `local-project/pm-vault/`
- Personal vault: `local-project/personal-project-notes/`

Start from the [Team vault](../../templates/team-vault/_README.md) and [Personal vault](../../templates/personal-vault/_README.md) templates. The folder structure is explained in [Project workspace](../../templates/project-workspace/README.md).

For the system view, read the [Handbook](../../handbook/README.md).

## Common mistakes

- **Opening a single file instead of a vault.** Links, search, and plugins only work on an open vault folder.
- **Copying only the visible files.** The `.obsidian` folder carries the plugins and settings. Copy the whole template.
- **Using one vault for both jobs.** Team visibility and private planning pull in different directions. Keep them separate.
- **Editing plugin-generated lines by hand.** dotpm and TaskNotes rewrite parts of their notes.
- **Treating personal notes as team commitments.** Promote work to the team vault when the team needs to see it.

## Next skill

Use [Project management](../project-management/README.md) to plan work in the team vault, or [Self-management](../self-management/README.md) to run your own execution in the personal vault.
