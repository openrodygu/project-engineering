# Links, properties, and dotpm

Links and properties are the two features that turn a folder of notes into a usable project workspace. dotpm depends on both.

## Links

Type `[[` to link another note in the same vault.

```markdown
[[Example Project]]
[[Alice|Alice's work]]
```

The **Backlinks** panel shows every note that links to the current note. In the team vault, project and task links make navigation and the graph view useful.

Links work inside one vault only. Use plain Markdown links for anything outside it:

```markdown
[Team vault](https://example.com/project)
```

## Properties

Properties are the block between `---` lines at the top of a note.

```yaml
---
title: Draft vendor comparison
status: in-progress
priority: high
due: 2026-11-20
tags:
  - vendor
---
```

Plugins read properties when the file changes. You can edit them in the **Properties** panel or in source mode.

## The two dotpm objects

dotpm uses two kinds of notes:

- **A project** has `pm-project: true` and lives in its own folder. It holds members, settings, saved views, and an ordered task list.
- **A task** has `pm-task: true` and lives in the project's `_tasks/` folder. It holds status, priority, dates, assignee, progress, parent, dependencies, and time data.

There is no separate subtask type. A subtask is a task whose `parentId` points at another task. A dependency is different: it says one task must happen before another.

## Create a team task

1. Open the **Project manager** pane.
2. Open **Example Project**.
3. Click **+ add task**.
4. Write a title that starts with a verb, for example "Draft vendor comparison".
5. Set status, priority, assignee, and a real due date.
6. Put context, links, and acceptance criteria in the description.
7. Save.

One file per task keeps sync conflicts rare and lets two people edit two different tasks without stepping on each other.

## Rules for hand editing

- Keep `id` unique. Do not copy a task file without changing it.
- Use `YYYY-MM-DD` for dates.
- Use status and priority values that exist in the settings.
- Do not edit generated task or project body lines. Put prose in the `description` property.
- Do not rename a task file by hand. Rename the title and let the plugin move it.

## Try it

Open the task you created in **Example Project** and add:

- A link to **Example Project** in the description.
- One dependency on another task.
- A clear next action in the description.

Then open the project table and confirm the task still appears and saves.

Next: [05 Bases and TaskNotes](05-bases-and-tasknotes.md)
