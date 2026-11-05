# Example Project case study

A generic project followed from kickoff to retrospective. It uses the [team vault](../templates/team-vault/) with dotpm for team visibility and the [personal vault](../templates/personal-vault/) with TaskNotes for personal execution.

## The project

**Outcome:** By January 16, deliver a tested prototype and a one-page recommendation that the sponsor accepts.

**Team:** Alice leads and owns scope. Bob researches options. Carol builds the prototype. Dave writes the summary and checks quality.

**Definition of done:**

- The prototype runs the agreed scenario.
- The recommendation states the choice, the cost, and the risk.
- The sponsor accepts the result.
- The final links and decisions are saved in the team vault.

**Constraints:** One short cycle, no new tooling, and only four people. The team agrees to keep the process small.

## Week 0 — kickoff

Alice writes the [project brief](../resources/templates/project-brief.md) and runs the [kickoff checklist](../resources/checklists/project-kickoff.md).

The brief fixes the outcome, the scope, the done criteria, and one milestone: a working prototype by January 14. Out of scope: production rollout, training, and a second use case.

The team agrees on three rules:

- The team vault is the shared view of record.
- Personal plans stay in personal vaults.
- Decisions that change the approach get a written record.

They create one project in dotpm with four tasks.

| Task | Owner | Start | Due | Status |
| --- | --- | --- | --- | --- |
| Define Scope | Alice | 2026-01-05 | 2026-01-09 | In Progress |
| Research Options | Bob | 2026-01-05 | 2026-01-07 | To Do |
| Build Prototype | Carol | 2026-01-08 | 2026-01-14 | To Do |
| Write Summary | Dave | 2026-01-15 | 2026-01-16 | To Do |

`Write Summary` depends on `Build Prototype`. The others can overlap.

## What lives where

| Item | Where | Why |
| --- | --- | --- |
| Outcome, scope, done criteria | Team vault project note | The team needs one shared definition |
| Task status and owners | Team vault, dotpm | Everyone can see the plan and the blockers |
| Dependency between build and summary | Team vault | It sets the order and the date |
| Decision on the chosen option | Team vault, decision record | The reasoning stays with the work |
| Alice's daily plan and private notes | Personal vault, TaskNotes | Execution detail does not need an audience |
| Bob's research notes | Personal vault, then a link in the task | Draft thinking stays private until it is useful |
| Source files | Git repository in `source/` | Changes need history and review |

The team does not copy the same commitment into both vaults. When a personal task becomes shared work, it is created once in the team vault and the personal note points to it.

## Week 1 — scope and research

Alice finishes `Define Scope` on January 6. She adds the acceptance criteria to the task description and links the brief. The task moves to `In Review`, then `Done` after the sponsor agrees.

Bob breaks `Research Options` into personal tasks in TaskNotes:

```text
TaskNotes
├── List three candidate options
├── Compare cost and risk
├── Write a one-page comparison
└── Share the recommendation with Alice
```

He keeps the draft comparison in his personal vault. When it is ready, he links it from the shared task and marks the task `Done`.

### Decision record

The team chooses one option on January 7. Alice writes a [decision record](../resources/templates/decision-record.md):

- **Context:** Three options fit the outcome. The team can only test one in the cycle.
- **Decision:** Test the smallest option that proves the core scenario.
- **Alternatives:** The faster option was rejected because it cannot be supported after the cycle. The more capable option was rejected because it does not fit the time.
- **Consequences:** The prototype will not cover every edge case, but it will produce a real recommendation on time.

The record lives in the shared vault next to the project. It is not rewritten later. If the choice changes, a new record supersedes it.

### Weekly review, January 9

Alice runs the [weekly review](../resources/checklists/weekly-review.md).

- `Define Scope` is done.
- `Research Options` is done.
- `Build Prototype` starts on January 8 with Carol.
- No tasks are overdue.
- One risk: Carol has less time than planned in week 2.
- Next week: finish the prototype, start the summary only when the prototype is accepted, and keep the review short.

She posts a [status update](../resources/templates/status-update.md):

> Overall: Green. Scope and research are done. Prototype is in progress. The summary depends on the prototype. No decisions needed this week.

## Week 2 — build and summary

Carol works from `Build Prototype` in the team vault. Her personal TaskNotes list holds the build steps and her focus blocks. The shared task holds only what the team needs: status, dates, and the acceptance criteria.

On January 12 the prototype hits a blocker: a test input is missing. Carol sets the task to `Blocked`, writes what she is waiting for, and names the person who can provide it. The blocker is visible in the team vault within the hour. Alice resolves it the same day, and the task returns to `In Progress`.

Dave does not start `Write Summary` early. The dependency is real. He uses the wait time to prepare the outline in his personal vault and to read the decision record.

### Status update, January 15

> Overall: Amber. The prototype is complete and accepted for the test scenario. The summary is in progress and due January 16. Risk: the sponsor has not seen the result yet. Decision needed: none. Ask: sponsor review on January 16.

The team finishes `Write Summary` on January 16. Dave links the recommendation from the project note and marks the task `Done`.

## Close

Alice runs the [project close checklist](../resources/checklists/project-close.md).

- The sponsor accepts the prototype and the recommendation.
- Every task is `Done`.
- Finished tasks are archived in dotpm.
- The decision record and final links stay in the project note.
- The team notes what is deliberately left out: production rollout and the second use case.

## Retrospective

The team answers four questions in 20 minutes.

1. **What went well?** The scope stayed small. The dependency between build and summary prevented rework. The blocker was visible quickly.
2. **What did not?** The sponsor saw the result late. The first status update was too optimistic about week 2 capacity.
3. **What did we learn?** One shared view was enough. Personal notes stayed useful without becoming a second plan.
4. **What will we keep, change, or drop?** Keep the brief, the weekly review, and the dependency. Change the first status update to name capacity risk earlier. Drop the daily check-in; the board was enough.

The team writes one change for the next project: add a sponsor review to the milestone, not only to the close.

## What made it work

- **One shared view.** The team could see status, owners, and the blocker without asking Alice.
- **One personal view per person.** Daily execution stayed private and light.
- **One real dependency.** It prevented Dave from starting too early.
- **One written decision.** The reasoning survived the cycle.
- **One short cadence.** A weekly review and one status update were enough.

## What to copy

- [Project brief](../resources/templates/project-brief.md)
- [Decision record](../resources/templates/decision-record.md)
- [Status update](../resources/templates/status-update.md)
- [Kickoff checklist](../resources/checklists/project-kickoff.md)
- [Weekly review](../resources/checklists/weekly-review.md)
- [Project close](../resources/checklists/project-close.md)
- [Team vault](../templates/team-vault/)
- [Personal vault](../templates/personal-vault/)
- [Project management](../guides/project-management/)
- [Self-management](../guides/self-management/)
