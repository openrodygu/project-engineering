# TaskNotes Guide

The practical playbook for **TaskNotes** in your personal vault.

TaskNotes is a task manager where each task is its own Markdown note, and every view is powered by Obsidian's **Bases** core plugin. This guide focuses on how we actually use it day to day, not on documenting every feature.

- New to Obsidian? Read [[Obsidian-Basics]] first.
- Personal onboarding: [[_README]]
- Planning techniques: [[Self-Management-101]]
- Shared vault rules: [[Shared-Vault-Boundary]]

---

## Start with the built-in tour

TaskNotes ships its own hands-on tutorial. Do that first; it is the fastest way to see the moving parts.

> [!tip] Do this once
> Open [[TaskNotes/Start Here|Start Here]] and work through it in place.
>
> The tour covers:
> - Creating a task from the command palette.
> - Converting inline checkboxes and bullets into tasks.
> - Opening the Task List, Agenda, Mini Calendar, Calendar, and Kanban views.
> - Adjusting settings only when they get in your way.
> - Adding a custom property.
> - Embedding views in other notes.
>
> When you finish, come back here. This guide is the playbook; the built-in tour is the orientation.

The official TaskNotes docs are the reference manual: <https://tasknotes.dev/obsidian/>.

---

## What this guide is for

The built-in tour shows you *what exists*. This guide shows you *what to do with it*:

- Capture work without breaking focus.
- Plan a day that is realistic.
- Run a focused work block.
- Track waiting and blocked work.
- Do a weekly reset.
- Promote team work to the shared vault.

If you only read one section, read the recipes.

---

## The six moves

| Move | What it means | TaskNotes feature |
| --- | --- | --- |
| **Capture** | Get it out of your head | Create new task, natural language, inline conversion |
| **Plan** | Decide what today actually is | Task List, `scheduled`, priorities |
| **Focus** | Do one thing at a time | Timer, Pomodoro, `In progress` |
| **Track** | Remember what is waiting | Contexts, `blockedBy`, task body |
| **Review** | Keep the list honest | Task List, Calendar, archive |
| **Promote** | Make team work visible | Manual handoff to the shared vault |

---

## What is already set up

This template ships with:

| Setting | Value |
| --- | --- |
| TaskNotes version | 4.16.1 |
| Bases core plugin | Enabled |
| Task folder | `TaskNotes/Tasks` |
| Archive folder | `TaskNotes/Archive` |
| Archive behavior | Tag-based by default (`archived` tag) |
| Task identification | Tag `task` |
| Views folder | `TaskNotes/Views` |
| Default status | `Open` |
| Default priority | `Normal` |
| Default scheduled date | Today |
| Natural language input | Enabled |
| Inline task conversion | Enabled |
| Inline converted task location | Beside the current note |
| Auto-create default Bases files | Enabled |
| Local API / MCP | Disabled |

Requirements: Obsidian **1.12.2 or newer**, Bases enabled, TaskNotes enabled.

---

## Recipes

### Capture a task in 10 seconds

**Command palette**

1. `Ctrl/Cmd+P`.
2. Run **TaskNotes: Create new task**.
3. Type a title. Press save.

New tasks land in `TaskNotes/Tasks` with status `Open`, priority `Normal`, and a scheduled date of today.

**Natural language**

Run **TaskNotes: Create new task** and type:

```text
Draft vendor comparison tomorrow at 2pm @office +ProjectAlpha #vendor high priority
```

- `@` suggests contexts.
- `#` suggests tags.
- `+` suggests project notes.
- `*` suggests statuses.

Natural language dates default to `scheduled`, not `due`. That is usually what you want.

**Inline conversion**

When a meeting note or daily note already contains the task:

```markdown
- [ ] Follow up with Vendor B about pricing
```

Convert it with the inline task action or the command palette. In this template, the converted task is created **beside the source note**, because the inline folder is set to `{{currentNotePath}}`.

**Quick actions**

Run **TaskNotes: Quick actions for current task** for a keyboard-searchable menu of status, priority, dates, time tracking, archive, and edit.

---

### Turn a note into actionable tasks

Use this when a note contains several follow-ups:

1. Write each follow-up as a checkbox or bullet.
2. Convert each line with inline conversion.
3. Open each task and add:
   - The next action.
   - A context.
   - A rough estimate.
   - A link to the project note, if any.

The source note stays as context. The tasks become real notes and appear in your views.

---

### Plan tomorrow in 5 minutes

1. Open the **Task List** view.
2. Filter to tasks scheduled today and overdue.
3. For each unfinished task, decide:
   - Reschedule it with `scheduled`.
   - Do it now if it is small.
   - Cancel it if it is no longer real.
4. Pick the top three for tomorrow.
5. Set their `scheduled` date to tomorrow.
6. Check the **Calendar** or **Agenda** view to see whether the day is realistic.

A good day has three real tasks, not twenty aspirational ones.

---

### Run a focused work block

1. Open the task you are actually doing.
2. Set status to `In progress`.
3. Start the task timer or a Pomodoro.
4. Work from the task body, not from the whole backlog.
5. When done, set status to `Done`.

Use the **Pomodoro** view if you want to see focus sessions and stats. Time tracking records sessions in `timeEntries`.

> [!tip] One thing at a time
> If five tasks are `In progress`, nothing is. Pick one and finish it.

---

### Track waiting and blocked work

When you are waiting on someone:

1. Add the `waiting` context or tag.
2. Use `blockedBy` to link the blocking task, if it exists.
3. Write the next action and the person who can unblock it in the task body.
4. Review `waiting` items during the weekly reset.

Example body:

```markdown
Waiting on: Vendor B pricing sheet.
Owner: <name>
Needed by: 2026-11-12
Next action: Follow up on 2026-11-10.
```

---

### Batch shallow work

Use contexts to group similar work:

- `office`
- `home`
- `deep-work`
- `admin`
- `email`
- `errands`
- `waiting`

Filter the Task List to one context and do that batch in one block. Context switching is expensive; batching is cheap.

---

### Set up a recurring chore

1. Create the task.
2. Set a recurrence in the task modal.
3. Use RRULE syntax if you are editing the property directly, for example:

```text
FREQ=WEEKLY;BYDAY=MO
```

Per-instance completion is tracked separately, so completing this week does not erase next week.

Good candidates: weekly review, timesheet, status update, recurring meeting prep.

---

### Do a weekly reset

1. Open the **Task List** and **Calendar**.
2. Clear overdue items: reschedule, do, or cancel.
3. Review `waiting` and nudge people.
4. Look at the week ahead. Is it realistic?
5. Archive completed tasks.
6. Promote anything that has become team work to the shared vault.
7. Pick the top three for Monday.

Fifteen to thirty minutes is enough. See [[Self-Management-101]] for the full checklist.

---

### Promote work to the shared vault

When a personal task becomes team work:

1. Open the shared vault (`../pm-vault`).
2. Create a matching task in **Example Project**.
3. Set status, priority, assignee, and dates.
4. Add a plain-text reference in your personal task:

   ```text
   Shared: Projects/Example Project/define-scope
   ```

5. Close or archive the personal task if it is only a pointer.

Full rules: [[Shared-Vault-Boundary]].

---

## Which view when

| View | Use it for |
| --- | --- |
| **Task List** | Daily triage and the weekly sweep |
| **Calendar** | Time blocking and seeing the shape of the week |
| **Agenda** | The next few days without the whole month |
| **Kanban** | Moving work through `Open` → `In progress` → `Done` |
| **Mini Calendar** | A compact calendar beside your notes |
| **Pomodoro** | Focus sessions and stats |

Open them with commands such as **TaskNotes: Open tasks view**, **Open kanban board**, **Open calendar view**, **Open agenda view**, or **Open mini calendar view**.

---

## Properties that actually matter

| Property | What it is for |
| --- | --- |
| `status` | Where the task is in your workflow |
| `priority` | What matters more when you have to choose |
| `scheduled` | When you plan to work on it |
| `due` | When it must be finished |
| `contexts` | Where or how you do it |
| `projects` | What larger outcome it belongs to |
| `timeEstimate` | How long you think it will take, in **minutes** |
| `blockedBy` | What must happen first |
| `recurrence` | Whether it repeats |
| `timeEntries` | Time you actually spent |

The most useful distinction is **scheduled vs. due**:

- `scheduled` is intent.
- `due` is a deadline.

Do not put a due date on everything. Fake deadlines create fake urgency.

---

## Current statuses and priorities

This template currently uses:

| Status | Meaning |
| --- | --- |
| **None** | No status set |
| **Open** | Not started |
| **In progress** | Actively working |
| **Done** | Finished |

| Priority | Meaning |
| --- | --- |
| **None** | No priority set |
| **Low** | Nice to have, or safe to slip |
| **Normal** | Default planned work |
| **High** | Important this cycle |

The shared vault uses a longer list. Mapping:

| Shared vault | Personal vault |
| --- | --- |
| To Do | Open |
| In Progress | In progress |
| Blocked | No direct equivalent; use a tag or note it in the description |
| In Review | No direct equivalent; use a tag or note it in the description |
| Done | Done |
| Cancelled | No direct equivalent; use a tag or note it in the description |
| Critical | High, or add a Critical priority |
| High | High |
| Medium | Normal |
| Low | Low |

If you want one vocabulary across both vaults, align them under **Settings → TaskNotes → Task Properties**. This guide does not change the setting for you.

---

## Archive

This template currently uses **tag-based archive**: archived tasks stay where they are and get the `archived` tag. Views can filter them out.

If you prefer folder-based archive, matching the shared vault's approach:

1. Open **Settings → TaskNotes → General**.
2. Enable **Move archived tasks to folder**.
3. Confirm the archive folder is `TaskNotes/Archive`.

Then archived tasks move to `TaskNotes/Archive`. Pick one behavior and stay consistent.

---

## Settings worth changing later

| Setting | Why |
| --- | --- |
| Statuses | Align with the shared vault if you want one vocabulary |
| Priorities | Align with the shared vault if you want one vocabulary |
| Folder for inline-created tasks | Centralize converted tasks in `TaskNotes/Tasks` |
| Move archived tasks to folder | Switch from tag-based to folder-based archive |
| Modal fields | Hide fields you never use |
| Calendar sync | Optional Google, Microsoft, or ICS integration |
| HTTP API / MCP | Optional; leave off unless you are automating |

---

## Troubleshooting

| Symptom | Fix |
| --- | --- |
| Views show errors or do not load | Enable **Bases** under Core plugins, then restart Obsidian |
| Views open the wrong file | Check **Settings → TaskNotes → General → Views & base files** |
| A new task does not appear | Confirm it has the `task` tag and is not in an excluded folder |
| A task appears in the wrong view | Open the `.base` file and inspect its filter or grouping rule |
| Changes are not reflected | Run **TaskNotes: Refresh cache**, then reopen the view |
| Archived tasks still appear | Check whether your views filter out the `archived` tag, or enable folder-based archive |
| Still stuck | Enable **Settings → TaskNotes → Features → Debug logging**, reproduce once, inspect the developer console |

---

## Reference

- Built-in tour — [[TaskNotes/Start Here|Start Here]]
- TaskNotes docs — <https://tasknotes.dev/obsidian/>
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
- [[Shared-Vault-Boundary]]
- [[Self-Management-101]]
- [[_README|Personal onboarding]]
