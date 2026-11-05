# Obsidian Basics

A short, practical introduction to Obsidian. Read this once, then use it as a reference.

This guide applies to your personal vault. The shared team vault is a separate Obsidian vault with its own guides.

- Personal onboarding: [[_README]]
- TaskNotes: [[TaskNotes-Guide]]
- Working with the team vault: [[Shared-Vault-Boundary]]
- Personal planning: [[Self-Management-101]]

---

## What Obsidian is

Obsidian is a Markdown editor that treats a folder on your computer as a **vault**. Every note is a `.md` file. Folders are real folders. Nothing is stored in a proprietary database.

Two ideas make Obsidian more than a text editor:

- **Links** — `[[Note name]]` connects notes. The **Backlinks** panel shows what links to the current note.
- **Properties** — structured `key: value` fields at the top of a note, also called YAML frontmatter. TaskNotes stores task data there.

Because notes are plain files, you can sync them with OneDrive, Obsidian Sync, iCloud, git, or any other file sync. You can also search, diff, and back them up without Obsidian.

---

## Install and open a vault

1. Download Obsidian from <https://obsidian.md>.
2. Install it and launch it.
3. On the start screen, choose **Open folder as vault**.
4. Select your personal vault folder.
5. If Obsidian asks whether you trust the author, choose **Trust author and enable plugins**.

Do not open a single file. Open the whole folder, so links, search, and plugins work.

### Switch between vaults

Obsidian can keep several vaults. Use the vault switcher in the bottom-left corner, or **Open another vault** from the start screen.

Your personal vault and the shared team vault are separate vaults. Switching between them does not merge them.

### Restricted mode and community plugins

Obsidian disables community plugins in **Restricted mode**. To use TaskNotes:

1. Open **Settings → Community plugins**.
2. Turn off **Restricted mode**.
3. Enable **TaskNotes**.

This template already has TaskNotes installed.

---

## The interface

| Area | What it does |
| --- | --- |
| Left ribbon | Vertical icon strip. TaskNotes adds icons here. |
| File explorer | The real folder tree of the vault. |
| Tab bar | Notes and views open as tabs. |
| Command palette | `Ctrl/Cmd+P`. The fastest way to run any command. |
| Quick switcher | `Ctrl/Cmd+O`. Jump to a note by name. |
| Search | `Ctrl/Cmd+Shift+F`. Search the whole vault. |
| Settings | `Ctrl/Cmd+,`. Vault and plugin options. |
| Right sidebar | Backlinks, outline, tags, properties. |

If you remember only one shortcut, remember the command palette. Every TaskNotes action is available there.

---

## Markdown in 60 seconds

```markdown
# Heading 1
## Heading 2

**bold** and *italic*

- bullet
- another bullet

1. numbered
2. list

- [ ] open checkbox
- [x] done checkbox

[external link](https://obsidian.md)
[[Internal note]] and [[Internal note|display text]]

> A quote or callout.
```

Markdown tables, fenced code blocks, and images also work. You do not need to be a Markdown expert. TaskNotes writes most of the structure for you.

### Callouts

Callouts are blockquotes with a type:

```markdown
> [!tip] Helpful
> This is a tip.

> [!warning] Careful
> This is a warning.
```

Obsidian renders them as colored boxes. They are useful for onboarding notes and reminders.

---

## Links, backlinks, and properties

### Links

- Type `[[` to link another note.
- Use `[[Note|label]]` to change the displayed text.
- Links only work inside one vault. A link here cannot open a note in the shared team vault, and the reverse is also true.

### Backlinks

The **Backlinks** panel lists every note that links to the current note. Linking tasks to project notes makes this useful.

### Properties

Properties are the block between `---` lines at the top of a note:

```yaml
---
title: Example task
status: open
due: 2026-11-20
contexts:
  - office
tags:
  - task
---
```

You can edit properties through Obsidian's **Properties** panel or directly in the source. TaskNotes reads them on file change.

Do not hand-edit TaskNotes properties unless you know the schema. See [[TaskNotes-Guide]] for the fields.

---

## Core plugins worth knowing

Obsidian ships with core plugins. These are already enabled in this template:

- **Search** — full-vault text and property search.
- **Quick switcher** — jump to a note by name.
- **Backlinks** and **Outgoing links** — navigate relationships.
- **Graph view** — see how notes connect.
- **Properties** — inspect structured data.
- **Bases** — turn notes into table, card, and calendar views. TaskNotes requires this.
- **Templates** — reusable note skeletons.
- **Daily notes** — one dated note per day, useful for a personal log.
- **File recovery** — Obsidian's local undo history.

Enable or disable core plugins under **Settings → Core plugins**.

---

## Vault hygiene

- **One note per topic.** Small notes link better than one giant note.
- **Use folders sparingly.** Links and search matter more than deep folder trees.
- **Keep names stable.** Renaming a note updates links if **Always update links** is on.
- **Do not edit the same note on two machines at once.** Sync tools can create conflict copies.
- **Back up the vault folder.** The vault is the backup target; there is no separate export step.
- **Do not place your personal vault inside the shared team vault.** Keep the two separate.

### Sync conflicts

If two devices edit the same file before sync resolves, the sync tool may create a conflict copy such as `Note.conflict-2026-11-04.md`. Diff the two files, keep the correct content, and delete the stale copy.

One note per task keeps conflicts rare, because two tasks are two files.

---

## Where to go next

- Personal onboarding: [[_README]]
- TaskNotes software guide: [[TaskNotes-Guide]]
- Shared vault rules: [[Shared-Vault-Boundary]]
- Personal planning: [[Self-Management-101]]
- Obsidian help: <https://help.obsidian.md>
