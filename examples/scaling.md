# Scaling

Multiple teams and projects change the coordination problem. The basics stay the same: one outcome per project, one owner per task, a current shared view, and written decisions. What changes is how many views and handoffs you need.

## What changes

| Area | Solo or small team | Multiple teams and projects |
| --- | --- | --- |
| Visibility | One team vault | A portfolio view plus one view per team |
| Ownership | One owner per task | One owner per project and one per team |
| Dependencies | Within one project | Across teams, projects, and dates |
| Decisions | One project log | Team logs plus a program decision log |
| Cadence | Weekly review | Team weekly, program biweekly, portfolio quarterly |
| Metrics | Team flow | Flow per team, never compared across teams |
| Standards | Team habits | Shared conventions with room for local practice |

## A portfolio view

Keep one list of projects. Five columns are enough.

| Project | Outcome | Owner | State | Next milestone |
| --- | --- | --- | --- | --- |
| Example Project | Tested prototype and recommendation | Alice | Active | Prototype, Jan 14 |
| Access Review | Remove stale accounts | Bob | Active | Audit complete, Feb 2 |
| Close Automation | Reduce close time | Carol | Proposed | Decision, Feb 10 |

The portfolio is not a detailed plan. It answers: what are we doing, who owns it, and what is next?

## Cross-project dependencies

A dependency that crosses a team needs four things:

- The work that is waiting.
- The work or decision it waits on.
- The owner on each side.
- The date it becomes a problem.

Put these in one shared list. Do not rely on two team boards to reveal the connection. A weekly program review is the place to check the list.

## Cadence

- **Team weekly:** each team runs its own [weekly review](../resources/checklists/weekly-review.md). Keep it under 30 minutes.
- **Program biweekly:** owners check cross-team dependencies, risks, and decisions. No status reading; read the updates before the meeting.
- **Portfolio quarterly:** review outcomes, stop work that no longer matters, and decide what to start.
- **Per project:** close with the [project close checklist](../resources/checklists/project-close.md) and a retrospective.

Meetings should produce a decision or a changed plan. If they produce only updates, use a written [status update](../resources/templates/status-update.md) instead.

## Decisions at two levels

- **Project decisions** stay with the project. Use the [decision record](../resources/templates/decision-record.md).
- **Program decisions** affect more than one team: shared standards, platform choices, priorities, and cross-team trade-offs. Keep these in one place that every owner can read.

Do not let a project decision quietly become a program decision. If it affects another team, move it to the program log and name the owners.

## Metrics

Track flow per team:

- Work in progress.
- Cycle time.
- Throughput.
- Overdue and blocked work.

Use the numbers to spot a local problem, not to rank teams. A team with a different kind of work will have different numbers. Comparing them invites the wrong behavior.

## Shared conventions

Agree on a small set of conventions that make handoffs cheap:

- The same status names.
- The same date format.
- The same definition of done.
- The same place for decisions.
- The same rule for what belongs in a shared view.

Let teams choose their own tools and local habits inside those conventions. Copying one team's full process into another team rarely survives contact with different work.

## What to add first

1. **A portfolio list.** One line per project, one owner, one next milestone.
2. **A cross-project dependency list.** Only real dependencies, with owners and dates.
3. **A program cadence.** Biweekly is usually enough.
4. **A shared decision log.** One place for choices that affect more than one team.
5. **One metric per team.** Pick the one that would change a decision.

Add these in order. Stop when the coordination problem is small enough.

## What stays the same

- One project has one outcome and a finish line.
- Every committed task has an owner.
- The shared view must match reality.
- Personal plans stay personal.
- Decisions keep their reasoning.
- Finished work is closed, archived, and reviewed.
- Add structure only when a real problem appears.

## Common failure modes

- The portfolio becomes a scoreboard.
- Every team is required to use the same board layout.
- Cross-team dependencies live only in chat.
- Program meetings multiply and produce no decisions.
- Metrics are compared across teams with different work.
- A large company's process is copied into a small group.

## Related

- [System canvas](../resources/system-canvas.md)
- [Weekly review](../resources/checklists/weekly-review.md)
- [Status update](../resources/templates/status-update.md)
- [Decision record](../resources/templates/decision-record.md)
- [Project management](../guides/project-management/)
- [Team lead](../guides/team-lead/)
- [Collaboration](../guides/collaboration/)
- [Handbook](../handbook/README.md)
