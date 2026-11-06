# Obsidian basics

A short, practical introduction to Obsidian. Read this once, then use it as a reference.

This is the repo-level guide. The team and personal vault templates ship their own `Obsidian-Basics.md` tuned to that vault. This page covers the shared basics and how to open the handbook itself.

- Read the handbook first: [START-HERE.md](../../START-HERE.md)
- The two-vault model: [01 Vaults and the two-vault model](01-vaults-and-the-two-vault-model.md)
- Open the templates: [02 Opening the templates](02-opening-the-templates.md)
- Templates overview: [templates/README.md](../../templates/README.md)

---

## Two ways to read this handbook

**In your browser.** You do not need to install anything. Open [START-HERE.md](../../START-HERE.md) and follow the links. Markdown renders on GitHub. Links written as `[[Note]]` appear inside `templates/` and only work when that folder is open in Obsidian.

**In Obsidian.** Install Obsidian, clone or download this repo, and open the repo folder as a vault. That gives you working links, backlinks, search, and the vault templates.

---

## What Obsidian is

Obsidian is a Markdown editor that treats a folder on your computer as a **vault**. Every note is a `.md` file. Folders are real folders. Nothing is stored in a proprietary database.

Two ideas make Obsidian more than a text editor:

- **Links** — `[[Note name]]` connects notes. The **Backlinks** panel shows what links to the current note.
- **Properties** — structured `key: value` fields at the top of a note, also called YAML frontmatter. Plugins such as dotpm and TaskNotes store their data there.

Because notes are plain files, you can sync them with OneDrive, Obsidian Sync, iCloud, Git, or any other file sync. You can also search, diff, and back them up without Obsidian.

---

## Install and open a vault

1. Download Obsidian from <https://obsidian.md>.
2. Install it and launch it.
3. On the start screen, choose **Open folder as vault**.
4. Select the folder you want:
   - **To read the handbook:** the repo folder you cloned or extracted.
   - **To use a template:** a copy of `templates/team-vault/` or `templates/personal-vault/` in your own workspace folder.
5. If Obsidian asks whether you trust the author, choose **Trust author and enable plugins**. The repo root needs this only if you add community plugins; the template copies already include them.

Do not open a single file. Open the whole folder, so links, search, and plugins work.

Open the repo root and a template copy as separate vaults. Do not open a template folder from inside the repo if you plan to edit it; copy it out first.

### Switch between vaults

Obsidian can keep several vaults. Use the vault switcher in the bottom-left corner, or choose **Open another vault** from the start screen.

Your team vault and personal vault are separate vaults. Switching between them does not merge them.

### Restricted mode and community plugins

Obsidian disables community plugins in **Restricted mode**. When it asks whether you trust the author, it is asking permission to run the community plugins bundled in the vault. Trusting the vault lets dotpm or TaskNotes run.

To use them:

1. Open **Settings → Community plugins**.
2. Turn off **Restricted mode**.
3. Enable the plugin you need.

The team vault template already has dotpm installed. The personal vault template already has TaskNotes installed. See the [team vault README](../../templates/team-vault/_README.md) and [personal vault README](../../templates/personal-vault/_README.md).

**Zero-trust option.** If you do not want to run the bundled plugins, delete `.obsidian/plugins/` from the vault copy, open the vault without enabling community plugins, then install dotpm or TaskNotes yourself from **Browse** in the same settings screen. The Markdown guides still work; the board and task views do not.

---

## The interface

| Area | What it does |
| --- | --- |
| Left ribbon | Vertical icon strip. Plugins add icons here. |
| File explorer | The real folder tree of the vault. |
| Tab bar | Notes and views open as tabs. |
| Command palette | `Ctrl/Cmd+P`. The fastest way to run any command. |
| Quick switcher | `Ctrl/Cmd+O`. Jump to a note by name. |
| Search | `Ctrl/Cmd+Shift+F`. Search the whole vault. |
| Settings | `Ctrl/Cmd+,`. Vault and plugin options. |
| Right sidebar | Backlinks, outline, tags, properties. |

If you remember only one shortcut, remember the command palette. Every plugin action is also available there.

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

Markdown tables, fenced code blocks, and images also work. You do not need to be a Markdown expert. dotpm and TaskNotes write most of the structure for you.

`[[wikilinks]]` are Obsidian syntax. They work inside one vault. On GitHub they appear as plain text; use the normal Markdown links in the repo docs when reading in a browser.

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
- Links only work inside one vault. A link in the team vault cannot open a note in the personal vault, and the reverse is also true.

### Backlinks

The **Backlinks** panel lists every note that links to the current note. Linking tasks to project notes makes this useful.

### Properties

Properties are the block between `---` lines at the top of a note:

```yaml
---
title: Example
status: in-progress
due: 2026-11-20
tags:
  - vendor
---
```

You can edit properties through Obsidian's **Properties** panel or directly in the source. Plugins read them on file change.

Do not hand-edit properties that a plugin generates unless you know the schema. See the template guides for the fields.

---

## Core plugins worth knowing

Obsidian ships with core plugins. These are enabled in the templates:

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
- **Keep names stable.** Renaming a note updates links if **Always update links** is on. External tools and scripts may still break.
- **Do not edit the same note on two machines at once.** Sync tools can create conflict copies.
- **Back up the vault folder.** The vault is the backup target; there is no separate export step.
- **Do not place your personal vault inside the team vault.** Keep the two separate.

### Sync conflicts

If two devices edit the same file before sync resolves, the sync tool may create a conflict copy such as `Note.conflict-2026-11-04.md`. Diff the two files, keep the correct content, and delete the stale copy.

One note per task keeps conflicts rare, because two tasks are two files.

---

## Where to go next

- [START-HERE.md](../../START-HERE.md) — the short orientation.
- [01 Vaults and the two-vault model](01-vaults-and-the-two-vault-model.md) — why team and personal work stay separate.
- [02 Opening the templates](02-opening-the-templates.md) — copy and open the team and personal vaults.
- [03 Markdown and notes](03-markdown-and-notes.md) — a little more Markdown.
- [templates/README.md](../../templates/README.md) — what each template includes.
- [Obsidian help](https://help.obsidian.md) — the official documentation.
