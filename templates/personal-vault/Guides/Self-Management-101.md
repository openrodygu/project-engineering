# Self-Management 101

A quick, practical guide to managing your own work. Not a formal system. Not a productivity religion. Just a loop that keeps your task list honest and your day sane.

Use what helps. Skip what does not.

- Personal onboarding: [[_README]]
- TaskNotes software: [[TaskNotes-Guide]]
- Team boundary: [[Shared-Vault-Boundary]]

---

## The mental model

Self-management is a loop, not a bigger backlog:

1. **Capture** what needs doing.
2. **Clarify** what it actually means.
3. **Choose** what matters today.
4. **Schedule** when you will do it.
5. **Do** the work.
6. **Review** and adjust.

Most task-list pain comes from skipping a step. Capture without clarify creates a junk drawer. Clarify without choose creates a guilt list. Choose without schedule creates a wish. Schedule without review creates drift.

---

## 1. Capture

Get it out of your head before it leaks.

Rules that work:

- **One inbox.** Use TaskNotes for everything you intend to track. Do not scatter tasks across notes, chat, and sticky notes.
- **Capture ugly.** A rough title is fine. You can clean it up later.
- **Do not organize while capturing.** Organizing is a different mode. Mixing them slows both down.
- **Capture the interruption.** If something pops into your head while you are working, write it down and go back to work.

In TaskNotes:

- Run **TaskNotes: Create new task** for a quick capture.
- Use natural language: `Email the vendor tomorrow @office +ProjectAlpha`.
- Convert a checkbox or bullet inline when a note already contains the task.

> [!tip] The two-minute rule
> If it takes less than two minutes, do it now instead of tracking it. Tracking has overhead. Do not pay it for trivia.

---

## 2. Clarify

A task is not a task until you know what "done" looks like.

For each item, answer:

- **Is it actionable?** If not, it is reference material or a note, not a task.
- **What is the next action?** "Plan the launch" is vague. "Draft the launch checklist" is actionable.
- **Where or how will I do it?** That is your context: `office`, `home`, `deep-work`, `waiting`.
- **How big is it?** Rough estimate in minutes.
- **What is it part of?** Link it to a project note if it belongs to a larger outcome.

Rules that work:

- **Verb first.** "Draft vendor comparison", not "Vendor comparison".
- **One next action per task.** If you cannot name the next action, the task is too vague.
- **Split anything over a few hours.** Large tasks hide problems and kill momentum.
- **Use the body for context.** Acceptance criteria, links, and notes go in the task note, not in your head.

In TaskNotes:

- Use the task body for context and links.
- Set `contexts` and `projects`.
- Set `timeEstimate` in minutes.
- Use `scheduled` for when you plan to work and `due` only for real deadlines.

---

## 3. Choose

You cannot do everything. Choosing is the job.

### The daily top three

Pick three tasks that would make today a good day. Not ten. Three.

- One that moves a real outcome forward.
- One that clears a commitment or unblocks someone.
- One that is small and satisfying, if the day allows.

### A quick Eisenhower pass

- **Urgent and important** — do it now.
- **Important, not urgent** — schedule it.
- **Urgent, not important** — batch it, delegate it, or question it.
- **Neither** — delete or archive it.

### A quick MoSCoW pass

- **Must** — today falls apart without it.
- **Should** — important, but there is a workaround.
- **Could** — nice to have.
- **Won't** — not today, and that is fine.

Rules that work:

- **Limit work in progress.** One or two active tasks at a time. Finish before starting.
- **Match energy, not just priority.** Put deep work in your best hours. Put shallow work in the gaps.
- **Protect the top three.** Everything else is optional.

In TaskNotes:

- Filter the Task List to today and overdue.
- Use priority as a tiebreaker, not a lifestyle.
- Use contexts to batch similar work.

---

## 4. Schedule

A task without a time is a hope.

Rules that work:

- **Use `scheduled` for intent.** When will you actually sit down with this?
- **Use `due` for deadlines.** Do not put a fake due date on everything.
- **Time-block the important work.** Put it on the calendar before the day fills itself.
- **Leave buffer.** Back-to-back blocks look productive and feel terrible.
- **Do not overbook.** A plan that assumes zero interruptions is fiction.

In TaskNotes:

- Set `scheduled` to today for tasks you intend to do today.
- Use the **Calendar** or **Agenda** view to see the shape of the week.
- Drag tasks to time blocks if you use timeblocking.
- Set `timeEstimate` so you can see when the day is full.

> [!warning] Scheduled is not the same as due
> A scheduled date is when you plan to work. A due date is when it must be finished. Mixing them creates unnecessary panic.

---

## 5. Do

The point of the system is to close the editor and do the work.

Rules that work:

- **Work from today's list.** Do not browse the whole backlog mid-task.
- **Batch shallow work.** Email, admin, and small follow-ups belong in one block, not sprinkled all day.
- **Use a focus timer if it helps.** Pomodoro is built in. Use it for deep work, not for meetings.
- **Stop when done.** "Done enough for today" is a real state.
- **Say no or defer.** A clear "not this week" is better than a silent yes.

In TaskNotes:

- Start a timer or Pomodoro on the task you are doing.
- Move the status to `In progress`.
- When finished, set it to `Done`.

> [!tip] One task at a time
> If you have five tasks in progress, you have five half-finished things. Pick one and finish it.

---

## 6. Review

A short review beats a perfect system you never use.

### Daily shutdown

Five minutes:

1. What did I finish?
2. What is still open?
3. What is the next action on each open item?
4. What am I doing first tomorrow?
5. Reschedule anything that slipped.

### Weekly reset

Fifteen to thirty minutes:

1. Open the Task List and Calendar.
2. Clear overdue items: reschedule, do, or cancel.
3. Check `waiting` items and nudge people.
4. Look at the week ahead. Is it realistic?
5. Archive completed work.
6. Promote anything that has become team work to the shared vault.

In TaskNotes:

- Use the **Task List** for the weekly sweep.
- Use the **Calendar** or **Agenda** for the week ahead.
- Archive completed tasks.
- Keep the backlog small enough to trust.

---

## Personal definition of done

Use a small checklist so "done" means something:

```markdown
- [ ] The deliverable exists where it should
- [ ] I checked it once with fresh eyes
- [ ] Anyone who needs it has been told
- [ ] No loose ends are hiding in the task body
- [ ] The task is marked Done, not 90 percent
```

If it is not done, say what is left. "90 percent for a week" is usually a sign the task was too big or the next action was unclear.

---

## Technique-to-TaskNotes cheat sheet

| Technique | Do this in TaskNotes |
| --- | --- |
| Capture | **TaskNotes: Create new task**, natural language, or inline conversion |
| Inbox | A saved Task List view filtered to untriaged tasks |
| Next action | Verb-first title plus a clear body |
| Context | `contexts` field |
| Project | `projects` field linking to a personal note |
| Estimate | `timeEstimate` in minutes |
| Daily top three | A saved view or a daily note list |
| WIP limit | Filter by `In progress` and keep the count low |
| Time blocking | `scheduled` plus the Calendar view |
| Deadline | `due`, used sparingly |
| Focus | Pomodoro or the task timer |
| Blocker | `blockedBy` or a `waiting` context |
| Daily shutdown | Reschedule open tasks, set tomorrow's first task |
| Weekly reset | Task List + Calendar sweep, then archive |
| Definition of done | Checklist in the task body |
| Retrospective | A short note linked from the project |

---

## Templates

### Daily plan

```markdown
## Today — YYYY-MM-DD

**Top three:**
1. ...
2. ...
3. ...

**Also today:**
- ...

**Waiting on:**
- ...

**First task tomorrow:**
- ...
```

### Weekly reset

```markdown
## Weekly reset — YYYY-MM-DD

- [ ] Cleared overdue tasks
- [ ] Reviewed waiting items
- [ ] Checked next week's calendar
- [ ] Archived completed tasks
- [ ] Promoted team work to the shared vault
- [ ] Picked the top three for Monday
```

### Personal retro

```markdown
## Retro — YYYY-MM-DD

**What worked:**
- ...

**What did not:**
- ...

**What I will change next week:**
- ...
```

---

## Common anti-patterns

| Anti-pattern | Why it hurts | Fix |
| --- | --- | --- |
| Capturing everything, clarifying nothing | The list becomes noise | Clarify the next action |
| Ten priorities | Nothing is a priority | Pick a daily top three |
| Five tasks in progress | Nothing finishes | Limit WIP |
| Fake due dates | Constant false urgency | Use `scheduled` for intent, `due` for real deadlines |
| One giant task | No momentum, no visibility | Split it into next actions |
| Never reviewing | The list drifts from reality | Daily shutdown and weekly reset |
| Perfect system, no work | Productivity theater | Close the app and do the task |
| Keeping everything forever | The backlog becomes a museum | Archive or delete |
| Tracking team work here only | The team cannot see it | Promote it to the shared vault |
| Editing two copies of one commitment | They drift | One authoritative copy |

---

## A few honest tips

- **Your task list is not your worth.** A long list is not a personality.
- **A small list you trust beats a big list you ignore.**
- **If you keep avoiding a task, it is probably vague, too big, or not actually yours.** Clarify, split, or drop it.
- **Plan for the day you will actually have,** not the one where everything goes right.
- **The best system is the one you will still use on a bad week.**

---

## Further reading

- Personal onboarding: [[_README]]
- TaskNotes software: [[TaskNotes-Guide]]
- Shared vault rules: [[Shared-Vault-Boundary]]
- Obsidian basics: [[Obsidian-Basics]]
- TaskNotes docs: <https://tasknotes.dev/obsidian/>
- Obsidian help: <https://help.obsidian.md>
