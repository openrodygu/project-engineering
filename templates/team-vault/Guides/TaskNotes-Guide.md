# TaskNotes Guide

Software tutorial for **TaskNotes**, the plugin for your **personal** Obsidian vault.

TaskNotes is a task manager where each task is its own Markdown note, and all views are powered by Obsidian's **Bases** core plugin. It is for your individual execution: your task list, daily plan, reminders, time blocking, and private notes.

This guide targets the stable **TaskNotes 4.x** release. TaskNotes 5 is in beta and is not covered here.

This guide is for the **personal vault only**. Team-visible work belongs in the shared dotpm vault; see [[dotpm-Guide]] and the team workflow in [[_README]].

- New to Obsidian? Read [[Obsidian-Basics]] first.
- Team planning techniques: [[Project-Management-101]]

---

## Why a separate personal vault

The shared vault answers: *what is the team doing, and where does it stand?*

Your personal vault answers: *what am I doing today, and how do I want to spend my time?*

Keeping them separate means:

- The team sees only commitments and status, not your private notes or daily planning.
- You can organize your personal vault however you like without disturbing the team.
- The shared vault stays small, current, and useful as a visual progress board.

There is no live sync between the two. A personal task becomes team work only when you manually create a matching dotpm task in the shared vault.

---

## Requirements

- Obsidian **1.12.2 or newer**.
- The **Bases** core plugin enabled. TaskNotes v4 views are `.base` files and will not open without Bases.
- TaskNotes installed from **Settings → Community plugins**.

Check Bases first:

1. Open **Settings → Core plugins**.
2. Confirm **Bases** is enabled.

---

## Set up your personal vault

1. Create a folder for your vault, for example `Documents/Obsidian/Personal`.
2. In Obsidian, choose **Open folder as vault** and select that folder.
3. Trust the author and enable plugins.
4. Enable **Bases** under **Settings → Core plugins**.
5. Open **Settings → Community plugins**, turn off Restricted mode, search for **TaskNotes**, install it, and enable it.
6. Open **Settings → TaskNotes → General** and confirm:
   - The task folder (default `TaskNotes/Tasks/`).
   - The views folder (default `TaskNotes/Views/`).
   - Task identification. Confirm how TaskNotes recognizes a task note (the default uses a task tag, commonly `#task`). Keep the default unless you have a reason to change it.
7. Open **Settings → TaskNotes → Task Properties** and review statuses and priorities. For consistency with the shared vault, use the same labels:
   - Statuses: To Do, In Progress, Blocked, In Review, Done, Cancelled.
   - Priorities: Critical, High, Medium, Low.
8. Run **TaskNotes: Open tasks view** from the command palette. If the view is missing, enable **Auto-create default files** under **Settings → TaskNotes → General**, or use the **Create files** button there.

Your personal vault is yours. Do not place it inside the shared team folder unless you intend to share it.

---

## How TaskNotes stores tasks

Each task is a Markdown note with YAML frontmatter. The body is free space for notes, checklists, links, and meeting notes.

```yaml
---
tags:
  - task
title: Review quarterly report
status: in-progress
priority: high
due: 2026-01-15
scheduled: 2026-01-14
contexts:
  - office
projects:
  - "[[Q1 Planning]]"
timeEstimate: 120
---
```

Key points:

- **One note per task.** No plugin database.
- **Frontmatter is the machine-readable layer.** The body is the human-readable layer.
- **Property names are configurable.** If you prefer different names, remap them in **Settings → TaskNotes → Task Properties**.
- **Tasks are normal notes.** Search, backlinks, graph, tags, and links all work on them.

### Task properties

| Property | Meaning |
| --- | --- |
| `title` | Task title, if not stored in the filename |
| `status` | Workflow state |
| `priority` | Critical, High, Medium, Low |
| `due` | Deadline |
| `scheduled` | When you plan to work on it |
| `contexts` | Where or how you do the work, such as `office`, `home`, `deep-work` |
| `projects` | Wikilinks to project notes in your personal vault |
| `tags` | Normal Obsidian tags, plus the task identification tag |
| `timeEstimate` | Estimate in **minutes** (dotpm uses hours) |
| `timeEntries` | Time tracking sessions |
| `recurrence` | RRULE for repeating tasks |
| `blockedBy` | Dependencies on other tasks |
| `reminders` | Relative or absolute reminders |

---

## Create tasks

### Task creation modal

1. Run **TaskNotes: Create new task** from the command palette.
2. Fill in title, status, priority, due date, scheduled date, contexts, projects, and estimate.
3. Save.

### Natural language

TaskNotes can parse plain English. For example:

```text
Review vendor pricing tomorrow at 3pm @office +ProjectAlpha #vendor high priority
```

- `@` suggests contexts.
- `#` suggests tags.
- `+` suggests project notes.
- `*` suggests statuses (the trigger is configurable).

### Inline conversion

You can convert an existing line in a note into a TaskNotes task. This works with checkboxes, bullets, numbered lists, blockquotes, headers, and plain text. Use the inline task command or the task context menu.

### Quick actions

Run **TaskNotes: Quick actions for current task** to open a keyboard-searchable palette for status, priority, dates, time tracking, archive, and edit.

---

## Views

All task views are `.base` files in `TaskNotes/Views/` and require Bases.

| View | Use it for |
| --- | --- |
| **Task List** | Day-to-day list with filters, sorting, and grouping |
| **Kanban** | Workflow by status, optionally with swimlanes |
| **Calendar** | Month, week, day, year, and list modes with drag-and-drop scheduling |
| **Agenda** | Short-horizon list of upcoming work |
| **Mini Calendar** | Compact month heatmap and fast navigation |
| **Pomodoro** | Focus intervals and session statistics |

Open them with commands such as **TaskNotes: Open tasks view**, **Open kanban board**, **Open calendar view**, **Open agenda view**, or **Open mini calendar view**. Each command points at a `.base` file; you can duplicate and customize those files.

### Filtering and grouping

Bases views filter and group on frontmatter properties. Common examples:

- Group the Task List by `status` or `priority`.
- Filter to `note.status != "Done"`.
- Sort by `due` ascending.
- Group Kanban by `status`.
- Show only tasks with a given context.

The `.base` files are plain text, so you can edit the YAML directly or use the Bases UI.

---

## Statuses, priorities, and projects

### Statuses

TaskNotes statuses are fully configurable under **Settings → TaskNotes → Task Properties → Statuses**. Each status has a label, color, and optional behavior.

For consistency, mirror the shared vault:

| Status | Meaning |
| --- | --- |
| **To Do** | Not started |
| **In Progress** | Actively working |
| **Blocked** | Waiting on something |
| **In Review** | Waiting for a check or sign-off |
| **Done** | Finished |
| **Cancelled** | Deliberately stopped |

You can enable **auto-archive** per status in TaskNotes. For example, archive tasks automatically a set number of minutes after they reach Done.

### Priorities

Priorities are configurable too. Use the same four labels as the shared vault so the two systems feel consistent:

- Critical
- High
- Medium
- Low

### Projects and contexts

- **Projects** are wikilinks to notes in your personal vault. Any note can act as a project anchor.
- **Contexts** describe where or how you work: `office`, `home`, `deep-work`, `errands`, `waiting`.
- Use contexts for personal planning; use projects for grouping related outcomes.

Do not try to link to the shared vault's project note. Wikilinks do not cross vaults. If you need a reminder, write a plain-text reference such as `Shared: Example Project / define-scope`.

---

## Time tracking, Pomodoro, and reminders

- **Time tracking** starts and stops a timer on a task and records sessions in `timeEntries`.
- **Pomodoro** runs focus intervals inside Obsidian and records completed sessions.
- **Reminders** can be relative to due or scheduled dates, or absolute date-times.
- **Recurring tasks** use RRULE syntax, for example `FREQ=WEEKLY;BYDAY=MO`. Per-instance completion is tracked separately.

These are personal productivity features. They do not feed the shared dotpm time tracking.

---

## Personal workflow

A simple loop that works:

### Capture

- Add anything to your task list as soon as it appears.
- Use the modal for structured tasks, or natural language for quick capture.
- Do not over-classify during capture.

### Plan the day

1. Open the **Task List** or **Agenda** view.
2. Filter to today and overdue.
3. Pick a small number of tasks to actually do.
4. Use `scheduled` for when you intend to work, and `due` only for real deadlines.

### Execute

- Work from the day's list, not from the entire backlog.
- Use Pomodoro or the timer if it helps you focus.
- Update status as you go.

### Close the day

- Mark finished tasks Done.
- Move unfinished tasks to a new scheduled date.
- Add a quick note to anything that changed.

### Review the week

- Open the Task List and Calendar.
- Clear overdue items: reschedule, do, or cancel.
- Archive completed work.
- Promote anything that has become a team commitment to the shared vault.

---

## Moving work between vaults

The systems are deliberately separate. There is no sync, no shared database, and no cross-vault links.

### Personal to shared

When a personal task becomes team work:

1. Open the shared dotpm vault.
2. Create a matching task in the relevant project, usually **Example Project**.
3. Set the assignee, status, priority, and dates.
4. In your personal TaskNotes task, add a plain-text reference such as `Shared: Example Project / define-scope`.
5. Close or archive the personal task if it is now only a pointer.

Create the shared task manually. Do not rely on importing TaskNotes notes across vaults; dotpm's TaskNotes import only works when both plugins see the same vault, which is not this setup.

### Shared to personal

When a shared task needs personal planning:

1. Keep the shared task as the team-visible source of truth.
2. Create a personal TaskNotes task for your own execution, with the same title and a plain-text reference to the shared task.
3. Update the shared task when your status changes; update the personal task for your own scheduling.

### The rule

One authoritative copy per commitment. The shared vault is authoritative for team-visible work. The personal vault is authoritative for your private execution. Do not let two copies drift while both are being edited.

---

## Troubleshooting

| Symptom | Fix |
| --- | --- |
| Views show errors or do not load | Enable **Bases** under Core plugins, then restart Obsidian |
| Views open the wrong file | Check **Settings → TaskNotes → General → Views & base files** |
| A new task does not appear | Confirm it matches the task identification setting and is not in an excluded folder |
| A task appears in the wrong view | Open the `.base` file and inspect its filter or grouping rule |
| Frontmatter looks wrong | Check the `---` delimiters and indentation; YAML is whitespace-sensitive |
| Changes are not reflected | Run **TaskNotes: Refresh cache**, then reopen the view |
| Still stuck | Enable **Settings → TaskNotes → Features → Debug logging**, reproduce once, inspect the developer console |

---

## Settings worth changing

| Setting | Why |
| --- | --- |
| Task folder | Keep personal tasks in one predictable place |
| Views folder | Keep `.base` files together |
| Task identification | Match how you tag or identify tasks |
| Statuses | Mirror the shared vault if you want consistency |
| Priorities | Mirror the shared vault if you want consistency |
| Auto-archive per status | Keep completed work out of active views |
| Modal fields | Hide fields you never use |
| Calendar sync | Optional Google, Microsoft, or ICS integration |
| HTTP API | Optional; leave off unless you are automating |

---

## Reference

- TaskNotes docs — <https://tasknotes.dev/obsidian/>
- TaskNotes core concepts — <https://tasknotes.dev/obsidian/core-concepts/>
- TaskNotes task management — <https://tasknotes.dev/obsidian/features/task-management/>
- TaskNotes views — <https://tasknotes.dev/obsidian/views/>
- TaskNotes settings — <https://tasknotes.dev/obsidian/settings/>
- TaskNotes troubleshooting — <https://tasknotes.dev/obsidian/troubleshooting/>
- TaskNotes source — <https://github.com/callumalpass/tasknotes>
- Obsidian Bases — <https://help.obsidian.md/bases>
- Obsidian help — <https://help.obsidian.md>

---

## Related guides

- [[Obsidian-Basics]]
- [[dotpm-Guide]]
- [[Project-Management-101]]
- [[_README|Team workflow]]
