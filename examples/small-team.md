# Small team

Three to five people. The goal is shared visibility without a heavy process. One shared view, one personal view per person, and a short weekly rhythm.

## The setup

- A [team vault](../templates/team-vault/_README.md) using dotpm for the shared plan.
- A [personal vault](../templates/personal-vault/_README.md) using TaskNotes for each person.
- A Git repository in `source/`.
- A project brief and a decision log in the team vault.

The team vault is the view of record. If work is not there, the team cannot see it. Personal vaults hold daily plans and private notes.

## Kickoff

Run the [project kickoff checklist](../resources/checklists/project-kickoff.md). Keep it to one hour.

- Agree on the outcome and the definition of done.
- Write the brief.
- Create the first milestone's tasks in the team vault.
- Give every task an owner and a status.
- Agree on the weekly review time.
- Agree on where decisions go.

A small team does not need a role for every activity. One person can own the board, another can run the review, and the work still belongs to the assignees.

## What lives where

| Item | Where |
| --- | --- |
| Outcome, scope, milestones | Team vault project note |
| Shared tasks and status | Team vault, dotpm |
| Blockers and dependencies | Team vault, with a stated waiting condition |
| Decisions | Team vault, decision record |
| Each person's daily plan | Personal vault, TaskNotes |
| Private notes and errands | Personal vault |

Promote work manually when it becomes shared. Do not keep two copies of the same commitment.

## The weekly rhythm

1. **Before the review:** each person updates their tasks and adds blockers.
2. **Review:** run the [weekly review](../resources/checklists/weekly-review.md). Check the board, overdue work, blockers, and the next milestone.
3. **Decide:** pick the few outcomes for next week and give each one an owner.
4. **After:** share a short [status update](../resources/templates/status-update.md) if anyone outside the team needs it.
5. **When a choice matters:** write a [decision record](../resources/templates/decision-record.md).

## A small team in motion

```text
Alice  → defines scope, owns the brief
Bob    → researches options, writes the comparison
Carol  → builds the prototype
Dave   → writes the summary and checks the result

Team vault: one project, one shared task list, four owners
Personal vaults: each person's daily plan and private notes
Git: source changes, one branch per task, reviewed before merge
```

## What to skip

- A status meeting every day.
- A separate tool for every activity.
- Story points compared across people.
- A perfect board before the first week.
- Roles that do not do anything.

## What to keep

- One shared view of record.
- One owner per task.
- A definition of done.
- A weekly review.
- A written decision log.
- A short retrospective at close.

## When to add structure

Add structure when:

- A second team depends on your dates.
- Work crosses team boundaries.
- The same decision keeps returning.
- The weekly review cannot fit in 30 minutes.

Then read [Scaling](scaling.md).

## Related

- [Project kickoff](../resources/checklists/project-kickoff.md)
- [Weekly review](../resources/checklists/weekly-review.md)
- [Status update](../resources/templates/status-update.md)
- [Team vault](../templates/team-vault/_README.md)
- [Personal vault](../templates/personal-vault/_README.md)
- [Project management](../guides/project-management/README.md)
- [Collaboration](../guides/collaboration/README.md)
