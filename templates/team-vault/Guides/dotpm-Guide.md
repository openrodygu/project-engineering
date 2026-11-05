# dotpm Guide

Software tutorial for **dotpm**, the plugin that runs the shared team vault.

dotpm is the Obsidian community plugin whose internal id is `project-manager` and whose display name is **dotpm**. It adds a project list, Table/Gantt/Board views, statuses, priorities, subtasks, dependencies, custom fields, saved views, time tracking, and archive.

This guide is for the **shared team vault only**. Personal task tracking uses TaskNotes in a separate vault; see [[TaskNotes-Guide]].

- New to Obsidian? Read [[Obsidian-Basics]] first.
- Team workflow: [[_README]]
- Optional planning techniques: [[Project-Management-101]]

---

## Install and enable

The shared vault already has dotpm installed in `.obsidian/plugins/project-manager/`. If it is not enabled:

1. Open **Settings → Community plugins**.
2. Turn off **Restricted mode**.
3. Find **dotpm** (listed in the community store as **Project Manager**) and enable it.
4. A **Project manager** ribbon icon appears on the left.

This vault runs dotpm **2.6.0**.

### What the plugin adds

- A project list.
- Table, Gantt timeline, and Kanban board views.
- Statuses, priorities, subtasks, dependencies, milestones, and custom fields.
- Saved views, time tracking, archive, and due-date reminders.
- A command palette set of actions.

---

## The two objects

**A project** is a note with `pm-project: true` in its properties, inside a folder of the same name. It is a container: it has members, custom fields, saved views, and an ordered list of top-level tasks. Projects do not have their own status or due date.

**A task** is a note with `pm-task: true` in its properties, inside the project's `_tasks/` folder. A task has a title, description, status, priority, start and due dates, progress, assignees, tags, a parent, subtasks, dependencies, and optional time data.

There is no separate "subtask" type. A subtask is a task whose `parentId` points at another task. Nesting can go as deep as you need.

### Why one file per task

- One change touches one file, so git diffs and sync conflicts stay small.
- You can search, grep, and edit tasks without Obsidian.
- Two people editing two different tasks never conflict.

---

## Where files live

```text
team-vault/                  shared team vault
├── _README.md                    team workflow
├── Guides/
│   ├── Obsidian-Basics.md
│   ├── dotpm-Guide.md            this guide
│   ├── TaskNotes-Guide.md
│   └── Project-Management-101.md
├── People/                       one note per team member
│   ├── Alice.md
│   ├── Bob.md
│   ├── Carol.md
│   └── Dave.md
├── Projects/
│   └── Example Project/
│       ├── Example Project.md            project note: settings and metadata
│       └── _tasks/
│           ├── define-scope.md   one file per task
│           ├── research-options.md
│           ├── build-prototype.md
│           ├── write-summary.md
│           └── Archive/          archived tasks live here
└── .obsidian/                    Obsidian and plugin configuration
```

Two rules about this layout:

- **Archive is a folder, not a flag.** Moving a task file into `_tasks/Archive/` archives it. Moving it out unarchives it.
- **The hierarchy lives in properties, not folders.** Every task in a project, at any depth, is a flat file in `_tasks/`. Parent and child are linked by IDs and wikilinks.

---

## The three views

Switch views with the control at the top of the task area.

| View | Use it for | Main actions |
| --- | --- | --- |
| **Table** | Day-to-day editing, filtering, bulk changes | Inline-edit status, priority, dates, progress; multi-select; save views |
| **Gantt** | Planning the timeline | Drag bars to reschedule, resize to change duration, draw dependencies, switch day/week/month/quarter/year |
| **Board** | Moving work through statuses | Drag cards between status columns; quick-add per column |

All three share the same filter bar and saved views. The **scope pill** beside the project name changes whether the view covers this project, this project plus sub-projects, a folder, or all projects.

### Table view

- Click a cell to edit status, priority, due date, progress, or title in place. `Enter` commits, `Escape` cancels.
- Click a row to open the full task editor.
- Use the column picker to show, hide, or reorder columns.
- Filter by text, status, priority, assignee, tag, due date, and archived state.
- Sort by clicking a column header.
- Select rows with the checkbox, `Shift+click` for a range, and `Ctrl/Cmd+click` to toggle one row.
- The bulk action bar can set status, priority, assignee, tag, due date, progress, or parent; it can also archive, unarchive, or delete.

### Gantt view

- Each task is a bar from start to due date. Milestones are diamonds.
- Drag the middle of a bar to move both dates; drag an edge to change duration.
- Hover a bar and use the right dot (output) and left dot (input) to draw a dependency.
- Switch granularity between day, week, month, quarter, and year.
- The today line marks the current date.
- `Escape` cancels dependency linking. `Ctrl/Cmd+Z` undoes a drag.

### Board view

- One column per status, in the order set in settings.
- Drag a card to another column to change its status.
- Use the **+** at the bottom of a column to quick-add a task in that status.
- By default only top-level tasks appear; subtask progress feeds a badge on the parent card.

---

## Statuses

These are the vault-wide statuses, in board order:

| Status | Meaning for this team |
| --- | --- |
| **To Do** | Not started. Ready to be picked up. |
| **In Progress** | Someone is actively working on it. |
| **Blocked** | Cannot move until something external is resolved. Say what in the description. |
| **In Review** | Work is done and waiting for a second pair of eyes or sign-off. |
| **Done** | Accepted and finished. Counts as complete. |
| **Cancelled** | Deliberately not doing it. Counts as complete, but not as delivered. |

`Done` and `Cancelled` are marked **complete** in dotpm. That means they stop due-date notifications and are skipped by auto-schedule.

A project can override the global list, but Example Project currently uses the global one. Keep the list short.

To customize statuses: **Settings → Project Manager → Task fields → Statuses**. Reorder by dragging; edit label, color, icon, and the complete flag; add or delete entries.

---

## Priorities

| Priority | Meaning |
| --- | --- |
| **Critical** | Drop other work. Blocks a commitment or a customer. |
| **High** | Must happen this cycle. |
| **Medium** | Normal planned work. The default. |
| **Low** | Nice to have, or can slip without escalation. |

Priority order drives sorting and the icon shown. Change a priority only when the consequence changes, not because work feels busy.

To customize priorities: **Settings → Project Manager → Task fields → Priorities**.

---

## Subtasks vs dependencies

These are different tools. Do not use one for the other.

- **Subtask** — this work is *part of* a larger task. Example: "Research Options" is part of "Define Scope". A parent's progress rolls up from its children.
- **Dependency** — this work is *ordered after* another task. Example: "Write Summary" depends on "Build Prototype". Dependencies draw arrows on the Gantt and drive auto-schedule.

### Subtasks

1. Open the parent task.
2. In **Subtasks**, click **+ add subtask**.
3. Type a title and press `Enter`.

You can also run **Create new subtask** from the command palette. A parent's progress is the average of its children's progress. Setting progress manually on a parent with children is allowed, but the rollup overwrites it when the tree changes.

### Dependencies

1. Open the task that is blocked.
2. In **Depends on**, pick the blocker.

The picker searches the whole vault, so dependencies can cross projects. Cycle protection is automatic. The **Blocks** row shows the reverse side: tasks waiting on this one.

### Auto-schedule

Auto-schedule is **on** in this vault. When you change a task's dates, its dependents move forward to keep the order valid.

- It only moves dates forward.
- It skips archived tasks and tasks in a complete status.
- It crosses project boundaries.
- A cycle is left alone rather than rescheduled into oblivion.
- **Pull dependents forward** is off by default; enable it only if you want early finishes to move dependents up.

Turn it off globally or per project if you need fully manual dates.

---

## Custom fields, saved views, time tracking, archive

### Custom fields

Custom fields add typed data to tasks: text, number, date, select, multi-select, person, checkbox, or URL.

- Define them for the whole vault under **Settings → Project Manager → Task fields → Custom fields**.
- Or define them on a project so its sub-projects inherit them.
- They appear in the task editor and as optional table columns.

Inheritance runs from the vault down through ancestors to the project. A project can hide an inherited field or override its name and type.

### Saved views

A saved view stores a filter + sort + view-mode combination under a name.

1. Set the filters, sort, and view you want.
2. Click **+ save view** above the table.
3. Name it after the question it answers.

Useful starter views: **My work**, **Overdue**, **Blocked**, **Due this week**, **Waiting for review**.

Views for a single project are stored in the project note. Views for a group of projects are stored in plugin settings.

### Time tracking

1. Open a task.
2. In **Time tracking**, set an **estimate** in hours.
3. Click **+ log time** and add date, hours, and a note.

The table's time column shows logged hours. The project overview shows logged vs. estimated. Logging is manual; batch it at the end of a work session.

### Archive

Archive moves finished or abandoned work out of the active views without deleting it.

- Right-click a task and choose **Archive**, or select several rows and use the bulk bar.
- Archived files live in `_tasks/Archive/`.
- Show archived tasks with the **Show archived** toggle in the filter bar.
- Unarchive by moving the file back, or use bulk **Unarchive**.
- Archiving a parent archives its whole subtree.

Prefer archive over delete.

---

## People notes

Assignees are picked from notes in `People/`. Each person note has a `color` property that tints their avatar. The notes for this team already exist:

- [[Alice]]
- [[Bob]]
- [[Carol]]
- [[Dave]]

To see everything assigned to a person, open their note and run **Show tasks assigned to this note**, or run **Show tasks assigned to a person** from the command palette.

---

## Everyday use

### Find your work

1. Open the **Project manager** pane and choose **Example Project**.
2. In the filter bar, set **Assignee** to your name.
3. Add a due-date filter such as **Overdue** or **This week**.
4. Save the combination as a view called **My work**.

### Update a task

- Fast path: click the status, priority, due date, or progress cell in the table and edit in place. `Enter` commits, `Escape` cancels.
- Full path: click the row to open the task editor, change fields, then **Save** or `Shift+Enter`.

Update status the same day something changes. A stale board is worse than no board.

### Capture a task

1. Click **+ add task** in the table or on a board column.
2. Write a title that starts with a verb: "Draft vendor comparison", not "Vendor comparison".
3. Set status, priority, assignee, and a due date if it is committed work.
4. Put context, links, and acceptance criteria in the description.

Quick capture is fine. You can fill in the rest later.

### Break work down

If a task is larger than about three days of work, break it into subtasks:

1. Open the task.
2. In **Subtasks**, click **+ add subtask**.
3. Write each child as a deliverable, not an activity.
4. Let progress roll up from the children.

### Finish and archive

When work is accepted, set it to **Done**. At the end of a sprint or release:

1. Filter to **Done**.
2. Select all.
3. Choose **Archive**.

The files move to `_tasks/Archive/` and leave the active views. Nothing is deleted.

---

## Keyboard and commands

dotpm ships with **no default hotkeys**, by Obsidian policy. Assign your own under **Settings → Hotkeys**.

### Keys that always work

| Context | Key | Action |
| --- | --- | --- |
| Table | `Enter` | Open the focused task, or commit an inline edit |
| Table | `Escape` | Cancel an edit or clear the selection |
| Table | `Shift+click` | Select a range of rows |
| Table | `Ctrl/Cmd+click` | Add or remove one row from the selection |
| Gantt | `Escape` | Cancel dependency linking |
| Gantt | `Ctrl/Cmd+Z` | Undo the last drag |
| Task editor | `Shift+Enter` | Save |
| Task editor | `Escape` | Close (and save, if save-on-close is on) |
| Any inline editor | `Enter` / `Escape` | Commit / cancel |

### Commands worth a hotkey

Open the command palette and search for these:

- **Create new task** — the one most people use constantly.
- **Open projects pane**
- **Create new subtask**
- **Open all projects in one view**
- **Show tasks assigned to a person**
- **Rebuild project index**

---

## Data safety and troubleshooting

### Hand-editing rules

You can open any project or task in a text editor, but:

1. **IDs must be unique.** Do not copy a file without changing its `id`.
2. **Dates are `YYYY-MM-DD`.** Use `""` for unset, not `null`.
3. **Status and priority IDs must exist** in the global or project list. Unknown IDs stay visible but lose their color and completion behavior.
4. **Project and task bodies are partly generated.** The heading, description, and task/subtask lists are rewritten on save. Put prose in the `description` property, not the project body.

### Common problems

| Symptom | Fix |
| --- | --- |
| Project missing from the list | Confirm `pm-project: true` in its properties; check **Excluded folders**; run **Rebuild project index** |
| Task missing from a view | Check the filter, the scope pill, and the **Show archived** toggle |
| Status colors look wrong | Confirm the task's status ID matches the current status list; reload the plugin |
| Duplicate or stale entries after moving files | Run **Rebuild project index** |
| Sync conflict | Treat `*.conflict-*.md` like any Obsidian conflict: diff, merge, delete the stale copy |
| Task will not save | The filename slug probably collides with another task. Change the title slightly |

### Sync and backup

The shared vault lives in a shared folder. One file per task keeps conflicts rare. If two machines edit the same task before sync resolves, a conflict copy may appear; merge it like any other conflict.

To back up, back up the vault folder. There is no separate export step.

### Mobile

dotpm works on iOS and Android. Gantt dragging and multi-select are easier on desktop; use the table and board on mobile.

---

## Optional power workflows

These are not required for day-to-day use.

- **Share a view** — run **Export current view as HTML** to write the open table, timeline, or board to a single file that opens in any browser.
- **Local API / MCP** — dotpm can serve the vault over `127.0.0.1` for scripts and coding agents. This is **disabled** in this vault (`localApiEnabled: false`). If you enable it under **Settings → Local API**, treat the bearer token as a secret and never commit it.
- **CLI** — `npm install -g @dotpm/cli` installs the `dotpm` command for querying and editing tasks from a terminal.

Do not enable the local API on a shared or untrusted machine without understanding the token.

---

## Settings currently in use

| Setting | Value |
| --- | --- |
| Default task view | Table |
| Gantt granularity | Week, labeled by week number |
| Auto-schedule | On |
| Save task on close | On |
| Task editor | Modal |
| Project opens in | Overview |
| Local API | Off |
| Theme | Border |

---

## Reference

- dotpm docs — <https://dotpm.pm/docs/install>
- dotpm website — <https://dotpm.pm>
- dotpm source and issues — <https://github.com/dotpm/obsidian-pm>
- Obsidian help — <https://help.obsidian.md>
- Team workflow — [[_README]]
- Personal task tracking — [[TaskNotes-Guide]]
- Optional planning techniques — [[Project-Management-101]]
