# Team Vault — Shared Project Vault

This is the team's shared Obsidian vault: a live, visual picture of what we are working on, what is blocked, and what is done. It is hosted in a shared drive and built on **dotpm**.

It supplements actual project management. It is not the system of record for scope, budget, contracts, or formal commitments. It is the team's shared view.

Each developer also keeps a **personal** Obsidian vault using **TaskNotes** for individual task tracking. The two systems are deliberately separate.

> [!tip] New here?
> Read this page, then [[Obsidian-Basics]], [[dotpm-Guide]], and [[TaskNotes-Guide]]. [[Project-Management-101]] is optional reference material.

---

## The two-vault model

| | Shared vault (this one) | Personal vault (yours) |
| --- | --- | --- |
| **Purpose** | Team visibility and coordination | Your individual execution |
| **Tool** | dotpm | TaskNotes |
| **Visibility** | Whole team | Private to you |
| **Source of truth for** | What the team is doing and its status | Your daily plan, personal tasks, reminders |
| **Location** | Shared drive | A folder you choose |
| **Contains** | Projects, tasks, dependencies, milestones, decisions | Personal tasks, contexts, time blocks, private notes |

### The shared vault

- Shows what the team has agreed to work on.
- Tracks status, progress, blockers, dependencies, and milestones.
- Holds team-facing notes, decisions, and links.
- Is the place to check when you want to know where a project stands.

### The personal vault

- Holds your own task list and daily plan.
- Tracks personal reminders, contexts, time blocking, and focus sessions.
- Can be organized however you like.
- Is not shared with the team.

### The rules

- **The shared vault is the team's view of record.** If work is not here, the team cannot see it.
- **The personal vault is yours.** Keep private notes and personal planning there.
- **No live sync.** Nothing moves between the two vaults automatically.
- **No cross-vault links.** Obsidian wikilinks do not work across vaults.
- **Promote manually.** When personal work becomes team work, create a matching dotpm task in the shared vault.
- **One authoritative copy.** Do not keep editing two copies of the same commitment in both systems.
- **The personal vault supplements the shared vault.** It does not replace it, and the shared vault does not replace actual project management.

```text
              shared team vault (dotpm)
              team-visible plan and status
                        |
          manual promotion when work becomes shared
                        |
        +---------------+---------------+
        |               |               |
  personal vault  personal vault  personal vault
   (TaskNotes)     (TaskNotes)     (TaskNotes)
   your execution  your execution  your execution
```

---

## What belongs where

| Item | Where it goes | Why |
| --- | --- | --- |
| A deliverable the team is counting on | Shared vault | The team needs to see it |
| A status change on shared work | Shared vault | Keeps the picture current |
| A blocker affecting the team | Shared vault, status **Blocked** | Makes the problem visible |
| A decision the team needs to know | Shared vault | Keeps context with the work |
| A dependency or milestone | Shared vault | Drives the timeline and the view |
| Your daily plan | Personal vault | Private execution detail |
| A personal reminder or errand | Personal vault | Not team work |
| Private notes or research | Personal vault | Yours alone |
| A follow-up you have not committed to yet | Personal vault | Promote it only if it becomes team work |

When in doubt: if the team needs to see it to coordinate, put it in the shared vault. If it is only about how you spend your own time, keep it personal.

---

## How work moves through the shared vault

1. **Capture.** Anyone can add a task to the relevant project.
2. **Assign.** Put a person on it when it is owned. Unassigned tasks are allowed, but visible.
3. **Update.** Change status, progress, and dates as reality changes.
4. **Close.** Set it to **Done** or **Cancelled**.
5. **Archive.** Clear finished work out of the active views at the end of a cycle.

There are no formal roles and no required ceremonies. The assignee is the person doing the work, not a title.

### Capture a task

1. Open the **Project manager** pane and choose **Example Project**.
2. Click **+ add task**.
3. Write a title that starts with a verb: "Draft vendor comparison", not "Vendor comparison".
4. Set a status, priority, assignee, and a real due date if it is committed.
5. Put context, links, and acceptance criteria in the description.

### Update a task

- Click the status, priority, due date, or progress cell in the table and edit in place.
- Click the row to open the full editor for description, subtasks, dependencies, custom fields, and time tracking.
- Update status the same day it changes. A stale view is worse than no view.

### Close and archive

When work is accepted, set it to **Done**. At the end of a sprint or release, filter to **Done**, select all, and choose **Archive**. The files move to `_tasks/Archive/`; nothing is deleted.

---

## Keeping the view honest

The shared vault is only useful if it reflects reality.

- **Update status when it changes.** Do not wait for a meeting.
- **Blocked needs a reason.** Say what you are waiting for and who can unblock it.
- **Use real dates.** Leave a date empty rather than inventing one.
- **Use subtasks for breakdown, dependencies for order.** They are different tools.
- **Prefer archive over delete.** Archive keeps history without cluttering the view.
- **Do not duplicate ongoing work.** One shared task per commitment.
- **Do a weekly glance if it helps.** Filter **Overdue**, **Blocked**, and **Due this week**. Five minutes is enough. It is a suggestion, not a required meeting.

---

## Statuses

| Status | Meaning for this team |
| --- | --- |
| **To Do** | Not started. Ready to be picked up. |
| **In Progress** | Someone is actively working on it. |
| **Blocked** | Waiting on something external. Write the blocker in the description. |
| **In Review** | Work is done and waiting for a check or sign-off. |
| **Done** | Accepted and finished. |
| **Cancelled** | Deliberately not doing it. |

`Done` and `Cancelled` count as complete in dotpm: they stop due-date reminders and are skipped by auto-schedule.

## Priorities

| Priority | Meaning |
| --- | --- |
| **Critical** | Blocks a commitment or a customer. |
| **High** | Should happen this cycle. |
| **Medium** | Normal planned work. |
| **Low** | Nice to have, or safe to slip. |

If everything is Critical, nothing is. See [[dotpm-Guide]] for how to change statuses and priorities.

---

## Team conventions

- **One project per outcome.** "Example Project" is a project because it has a finish line. "Automation" would be a theme, not a project.
- **Use sub-projects for workstreams** inside a large outcome.
- **Task titles start with a verb** and name the deliverable. Keep them unique inside a project; duplicate titles collide on filenames.
- **Assignees are person notes**, not free text. Use the picker.
- **Dates are always `YYYY-MM-DD`.** Leave a date empty rather than inventing one.
- **Tags are lowercase, short, and reused.**
- **Put context in the description.** Add acceptance criteria, links, decisions, and blockers there.
- **Do not put prose in a project note's body.** dotpm regenerates it. Use the project's `description` property instead.
- **Do not edit generated `## Tasks`, `## Subtasks`, or `Project:`/`Parent:` lines.** The plugin rewrites them.
- **Do not rename a task file by hand.** Rename the title and let the plugin move the file.
- **Do not copy a task file without changing its `id`.**
- **Do not delete unless you mean it.** Archive first.

Because this vault lives in a shared folder, avoid editing the same task from two machines at once. One file per task keeps conflicts rare; if a conflict copy appears, merge it like any other Obsidian conflict.

---

## Onboarding path

1. Read this page.
2. Read [[Obsidian-Basics]] if you are new to Obsidian.
3. Read [[dotpm-Guide]] for the shared vault.
4. Read [[TaskNotes-Guide]] and set up your personal vault.
5. Read [[Project-Management-101]] only if you want planning techniques. It is optional.
6. Open the **Example Project** project in the shared vault.
7. Filter the table to **Assignee = you** and look at what is assigned to you.
8. Open one task, read its description, set its status and progress, and save.

If the project list ever looks stale after moving files, run **Rebuild project index** from the command palette.

---

## Guide index

| Guide | Use it for | When |
| --- | --- | --- |
| [[Obsidian-Basics]] | Installing Obsidian, opening a vault, links, properties, core plugins | First, if Obsidian is new to you |
| [[dotpm-Guide]] | The shared vault: projects, tasks, views, statuses, dependencies, troubleshooting | Before your first task |
| [[TaskNotes-Guide]] | Your personal vault: install, tasks, views, daily workflow | When setting up personal tracking |
| [[Project-Management-101]] | Optional planning techniques, templates, anti-patterns | When you want more structure |

---

## Current project

### Example Project

A sample project that demonstrates how the team vault is organized.

- Project note: [[Example Project]]
- Team: [[Alice]], [[Bob]], [[Carol]], [[Dave]]
- Active work includes defining scope, researching options, building a prototype, and writing a summary.

Open the project from the **Project manager** pane, or click [[Example Project]].

---

## Support

- dotpm docs — <https://dotpm.pm/docs/install>
- TaskNotes docs — <https://tasknotes.dev/obsidian/>
- Obsidian help — <https://help.obsidian.md>
- dotpm source and issues — <https://github.com/dotpm/obsidian-pm>
- TaskNotes source — <https://github.com/callumalpass/tasknotes>

For a software problem, check the relevant guide's troubleshooting section first. For a data problem in the shared vault, run **Rebuild project index** before anything else.

---

## Vault map

| Path | What it holds |
| --- | --- |
| `_README.md` | This team workflow |
| `Guides/Obsidian-Basics.md` | General Obsidian tutorial |
| `Guides/dotpm-Guide.md` | Shared-vault software tutorial |
| `Guides/TaskNotes-Guide.md` | Personal-vault software tutorial |
| `Guides/Project-Management-101.md` | Optional planning reference |
| `Projects/Example Project/` | The Example Project project |
| `Projects/Example Project/_tasks/` | One Markdown file per task |
| `Projects/Example Project/_tasks/Archive/` | Archived tasks |
| `People/` | One note per team member |
| `.obsidian/` | Obsidian, theme, and dotpm configuration |
