# Shared Vault Boundary

How your personal vault relates to the shared team vault.

The short version: **the shared vault is for team visibility. This vault is for your own execution. They are separate on purpose.**

- Personal onboarding: [[_README]]
- TaskNotes software: [[TaskNotes-Guide]]
- Personal planning: [[Self-Management-101]]

---

## Where the shared vault is

The shared team vault is the sibling folder:

```text
your-workspace/
├── pm-vault/                  shared team vault (dotpm)
└── personal-project-notes/    your personal vault (TaskNotes)
```

From this vault, the shared vault is `../pm-vault`.

Open it as a separate Obsidian vault with **Open another vault**. Its own `_README.md` and `Guides/` explain the team workflow and the dotpm software.

Do not link to it with a wikilink. Wikilinks do not cross vaults. Use a plain-text path or a short reference instead.

---

## What lives in the shared vault

The shared vault uses **dotpm** and holds team-visible work:

- Projects, such as **Example Project**.
- Team tasks and subtasks.
- Status, progress, assignees, and due dates.
- Dependencies and milestones.
- Decisions and context the team needs.
- Blockers that affect other people.

If the team needs to see it to coordinate, it belongs in the shared vault.

## What lives here

This vault holds your private execution:

- Your task list and daily plan.
- Personal reminders and errands.
- Contexts, time blocks, and focus sessions.
- Private notes and research.
- Your own project anchors, if you use them.

If it is only about how you spend your own time, keep it here.

---

## The rules

- **No live sync.** Nothing moves between vaults automatically.
- **No cross-vault links.** A wikilink in one vault cannot open a note in the other.
- **Promote manually.** When personal work becomes team work, create a matching task in the shared vault.
- **One authoritative copy.** The shared vault is authoritative for team commitments. This vault is authoritative for your personal execution.
- **Do not duplicate ongoing work.** If a shared task exists, do not keep a second actively edited copy here.
- **Do not put private notes in the shared vault.** Keep personal context personal.
- **Do not rely on import.** dotpm's TaskNotes import only works when both plugins see the same vault. That is not this setup.

---

## Promoting a personal task

When a personal task becomes team work:

1. Open the shared vault (`../pm-vault`).
2. Open the **Project manager** pane and choose the relevant project, usually **Example Project**.
3. Click **+ add task** and create a matching task.
4. Set status, priority, assignee, and dates.
5. Put context, links, and acceptance criteria in the description.
6. In your personal task, add a plain-text reference such as:

   ```text
   Shared: Projects/Example Project/define-scope
   ```

7. Close or archive the personal task if it is now only a pointer.

If you are not sure whether something is team work, ask: *does anyone else need to see this to coordinate?* If yes, promote it.

---

## Keeping the two copies aligned

Once a task is shared, the shared vault is the source of truth for status.

- Update the shared task when the team-visible status changes.
- Keep the personal task for your own scheduling and execution.
- If the shared task is cancelled, close the personal task too.
- If the shared task is done, close the personal task.
- Do not report a different status in each place.

One commitment, one authoritative status. The shared vault wins for team-visible work.

---

## Status mapping

The shared vault and this template do not use identical status lists by default.

| Shared vault | Personal vault |
| --- | --- |
| To Do | Open |
| In Progress | In progress |
| Blocked | No direct equivalent; use a tag or note it in the description |
| In Review | No direct equivalent; use a tag or note it in the description |
| Done | Done |
| Cancelled | No direct equivalent; use a tag or note it in the description |

If you want the exact same vocabulary, align the lists under **Settings → TaskNotes → Task Properties → Statuses**. See [[TaskNotes-Guide]] for the steps. This template does not change the setting for you.

## Priority mapping

| Shared vault | Personal vault |
| --- | --- |
| Critical | High, or add a Critical priority |
| High | High |
| Medium | Normal |
| Low | Low |

You can align priorities the same way under **Settings → TaskNotes → Task Properties → Priorities**.

## Time estimates

- TaskNotes stores `timeEstimate` in **minutes**.
- dotpm stores `timeEstimate` in **hours**.

When you promote a task, convert:

| TaskNotes | dotpm |
| --- | --- |
| 30 | 0.5 |
| 60 | 1 |
| 120 | 2 |
| 240 | 4 |

---

## Opening both vaults

You can keep both vaults open in Obsidian at the same time, but they are separate windows or tabs depending on your setup.

- Use the vault switcher in the bottom-left corner.
- The shared vault will show the dotpm ribbon icon and project list.
- Your personal vault will show the TaskNotes views.

Switching vaults does not merge data. It is the same as switching projects.

---

## What not to do

| Don't | Why |
| --- | --- |
| Link to a shared note with `[[...]]` | Wikilinks do not cross vaults |
| Copy a shared task here and edit both | The two copies drift and nobody knows which is true |
| Put private notes in the shared vault | The whole team can see them |
| Use the shared vault for personal errands | It adds noise to the team view |
| Assume TaskNotes and dotpm sync | They do not; the handoff is manual |
| Rely on dotpm's TaskNotes import across vaults | It only works inside one vault |

---

## Quick checklist

Before you promote:

- [ ] Does the team need to see this?
- [ ] Is there already a shared task for it?
- [ ] Is the shared task the authoritative copy?
- [ ] Did I add a plain-text reference in my personal task?
- [ ] Did I close or archive the personal duplicate if it is only a pointer?

Before you update:

- [ ] Am I updating the shared task for team-visible status?
- [ ] Am I updating the personal task only for my own scheduling?
- [ ] Do both agree on whether the work is open or done?

---

## Related guides

- [[_README|Personal onboarding]]
- [[TaskNotes-Guide]]
- [[Self-Management-101]]
- [[Obsidian-Basics]]
