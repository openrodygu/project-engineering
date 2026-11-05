# Personal Vault — TaskNotes Template

This is a **personal** Obsidian vault template for team members. It is for your own task tracking, daily planning, and private notes.

It supplements the shared team vault. It does not replace it, and it does not replace actual project management.

> [!tip] Using this as a template
> Duplicate this folder, open the copy as your own vault, and rename it if you like. The `.obsidian` folder carries the TaskNotes setup, so the copy is ready to use.

---

## The two-vault model

|                         | Shared team vault                                      | Personal vault (this one)                            |
| ----------------------- | ------------------------------------------------------ | ---------------------------------------------------- |
| **Purpose**             | Team visibility and coordination                       | Your individual execution                            |
| **Tool**                | dotpm                                                  | TaskNotes                                            |
| **Visibility**          | Whole team                                             | Private to you                                       |
| **Source of truth for** | What the team is doing and its status                  | Your daily plan, personal tasks, reminders           |
| **Location**            | `your-workspace/team-vault/` *(any shared drive)* | A folder you choose                                  |
| **Contains**            | Projects, tasks, dependencies, milestones, decisions   | Personal tasks, contexts, time blocks, private notes |

### The shared vault

The shared vault is the folder `../team-vault` inside `your-workspace`. It uses dotpm and holds the team-visible plan.

Open it as a separate Obsidian vault when you need to see or update team work. Its own `_README.md` explains the team workflow.

### The personal vault

This vault is yours. It holds:

- Your task list and daily plan.
- Personal reminders and contexts.
- Time blocks and focus sessions.
- Private notes and research.

You can organize it however you like. It is not shared with the team.

### The rules

- **The shared vault is the team's view of record.** If work is not there, the team cannot see it.
- **The personal vault is yours.** Keep private notes and personal planning here.
- **No live sync.** Nothing moves between the two vaults automatically.
- **No cross-vault links.** Obsidian wikilinks do not work across vaults.
- **Promote manually.** When personal work becomes team work, create a matching task in the shared vault.
- **One authoritative copy.** Do not keep editing two copies of the same commitment in both systems.
- **The personal vault supplements the shared vault.** It does not replace it.

---

## What belongs where

| Item | Where it goes | Why |
| --- | --- | --- |
| A deliverable the team is counting on | Shared vault | The team needs to see it |
| A status change on shared work | Shared vault | Keeps the team picture current |
| A blocker affecting the team | Shared vault, status **Blocked** | Makes the problem visible |
| A decision the team needs to know | Shared vault | Keeps context with the work |
| A dependency or milestone | Shared vault | Drives the team timeline |
| Your daily plan | Personal vault | Private execution detail |
| A personal reminder or errand | Personal vault | Not team work |
| Private notes or research | Personal vault | Yours alone |
| A follow-up you have not committed to yet | Personal vault | Promote it only if it becomes team work |

When in doubt: if the team needs to see it to coordinate, put it in the shared vault. If it is only about how you spend your own time, keep it personal.

---

## First run

1. Duplicate this folder for yourself if you are using it as a template.
2. In Obsidian, choose **Open folder as vault** and select your copy.
3. Trust the author and enable plugins.
4. Confirm **Bases** is enabled under **Settings → Core plugins**.
5. Confirm **TaskNotes** is enabled under **Settings → Community plugins**.
6. Run **TaskNotes: Open tasks view** from the command palette.
7. Open [[TaskNotes/Start Here|Start Here]] for the built-in hands-on tour.
8. Create your first task with **TaskNotes: Create new task**.

If the TaskNotes views are missing, enable **Auto-create default files** under **Settings → TaskNotes → General**, or use the **Create files** button there.

---

## The daily loop

1. **Capture.** Add anything that needs doing to your task list.
2. **Clarify.** Decide the next action, context, and rough estimate.
3. **Choose.** Pick a small number of tasks for today.
4. **Schedule.** Put them on the calendar or set a scheduled date.
5. **Do.** Work from today's list, not the whole backlog.
6. **Review.** Close the day, reschedule what slipped, and clear the noise.

See [[Self-Management-101]] for the longer version with tips and templates.

---

## Personal conventions

- **One task per note.** TaskNotes creates a Markdown file for each task.
- **Dates are `YYYY-MM-DD`.** Leave a date empty rather than inventing one.
- **Estimates are in minutes** in TaskNotes. The shared vault uses hours.
- **Contexts are lowercase and reused.** Examples: `office`, `home`, `deep-work`, `waiting`.
- **Projects are wikilinks to your own project notes.** Any note can be a project anchor.
- **Do not link to the shared vault.** Use plain text references instead.
- **Keep the task identification tag.** This vault uses the `task` tag.
- **Archive instead of deleting.** Archive behavior is described in [[TaskNotes-Guide]].
- **Do not put team commitments here.** Use the shared vault for those.

---

## Promoting work to the shared vault

When a personal task becomes team work:

1. Open the shared vault (`../team-vault`).
2. Open the **Project manager** pane and choose the relevant project, usually **Example Project**.
3. Create a matching task with the same title.
4. Set status, priority, assignee, and dates.
5. Put context and acceptance criteria in the description.
6. In your personal task, add a plain-text reference such as `Shared: Projects/Example Project/define-scope`.
7. Close or archive the personal task if it is now only a pointer.

Do not rely on sync or import between vaults. The handoff is manual by design. See [[Shared-Vault-Boundary]] for the full rules.

---

## Guide index

| Guide | Use it for | When |
| --- | --- | --- |
| [[Obsidian-Basics]] | Installing Obsidian, opening a vault, links, properties, core plugins | First, if Obsidian is new to you |
| [[TaskNotes-Guide]] | Actionable TaskNotes recipes, views, statuses, archive, troubleshooting | Before your first task |
| [[Shared-Vault-Boundary]] | How this vault relates to the team vault, promotion, mapping | Before you promote anything |
| [[Self-Management-101]] | Personal planning techniques, tips, templates, anti-patterns | When you want more structure |

The built-in [[TaskNotes/Start Here|Start Here]] tour is also worth doing once.

---

## Vault map

| Path | What it holds |
| --- | --- |
| `_README.md` | This personal onboarding |
| `Guides/Obsidian-Basics.md` | General Obsidian tutorial |
| `Guides/TaskNotes-Guide.md` | Personal-vault software tutorial |
| `Guides/Shared-Vault-Boundary.md` | Rules for working with the team vault |
| `Guides/Self-Management-101.md` | Personal planning techniques |
| `TaskNotes/Start Here.md` | Built-in TaskNotes tour |
| `TaskNotes/Tasks/` | Task notes, created on first task |
| `TaskNotes/Archive/` | Archive target if folder-based archive is enabled |
| `TaskNotes/Views/` | Bases views for TaskNotes |
| `.obsidian/` | Obsidian, theme, and TaskNotes configuration |

---

## Support

- TaskNotes docs — <https://tasknotes.dev/obsidian/>
- TaskNotes troubleshooting — <https://tasknotes.dev/obsidian/troubleshooting/>
- Obsidian help — <https://help.obsidian.md>
- TaskNotes source — <https://github.com/callumalpass/tasknotes>

For a TaskNotes problem, check [[TaskNotes-Guide]] first. For a shared-vault problem, open the shared vault and read its `_README.md` and dotpm guide.
