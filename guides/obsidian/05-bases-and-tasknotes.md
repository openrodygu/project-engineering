# Bases and TaskNotes

TaskNotes is the personal task tool in this workspace. It stores one Markdown file per task and uses Obsidian's **Bases** core plugin for every view.

## What Bases does

Bases turns notes into table, card, and calendar views based on their properties. It does not move data. It reads the properties already in your notes and displays them in different shapes.

Enable it under **Settings → Core plugins → Bases**. The personal vault template has it on already.

## What a TaskNotes task is

A task is a note with the `task` tag. Its properties carry the useful data:

| Property | Meaning |
| --- | --- |
| `status` | Where the task is in your workflow |
| `priority` | What matters when you have to choose |
| `scheduled` | When you plan to work on it |
| `due` | When it must be finished |
| `contexts` | Where or how you do it |
| `projects` | What larger outcome it belongs to |
| `timeEstimate` | How long you think it takes, in minutes |
| `blockedBy` | What must happen first |

The most useful distinction is **scheduled vs. due**. Scheduled is intent. Due is a deadline. Do not put a due date on everything.

## The views

| View | Use it for |
| --- | --- |
| **Task List** | Daily triage and the weekly sweep |
| **Calendar** | Time blocking and the shape of the week |
| **Agenda** | The next few days without the whole month |
| **Kanban** | Moving work from Open to In progress to Done |
| **Mini Calendar** | A compact calendar beside your notes |
| **Pomodoro** | Focus sessions and time tracking |

Open them from the command palette, for example **TaskNotes: Open tasks view** or **TaskNotes: Open agenda view**.

## Create a personal task

1. Press `Ctrl/Cmd+P`.
2. Run **TaskNotes: Create new task**.
3. Type a clear title.
4. Add a context such as `office` or `deep-work`.
5. Add an estimate in minutes.
6. Set a scheduled date for tomorrow.
7. Save.

Natural language works too:

```text
Draft vendor comparison tomorrow at 2pm @office +Example high priority
```

`@` suggests contexts, `#` suggests tags, `+` suggests project notes, and `*` suggests statuses. Natural language dates default to `scheduled`, which is usually what you want.

## TaskNotes is not the team vault

Do not put team commitments only in TaskNotes. The team cannot see them. When a personal task becomes team work, create a matching dotpm task in the team vault and leave a plain-text reference in the personal task.

## Try it

Create one personal task scheduled for tomorrow with:

- One context.
- A 30-minute estimate.
- A link to a project note in the personal vault.

Then open the **Calendar** or **Agenda** view and confirm the task appears on the right day.

Next: [06 Plugins and themes](06-plugins-and-themes.md)
