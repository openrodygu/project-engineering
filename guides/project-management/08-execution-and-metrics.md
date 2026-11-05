# Execution and metrics

Run the work from the board, keep status honest, and use a few measures that change decisions.

## Execute from one source

The team board is the authoritative view of committed work. If a task is not on the board, the team cannot see it. If the board is stale, the team cannot trust it.

Rules that work:

- Update status the day it changes.
- Aim for one task in progress per person unless the work genuinely interleaves.
- Move work to Done when it is accepted, not when it is nearly finished.
- Write the blocker when you set Blocked, and name who can remove it.

In dotpm, use the Board view for flow and the Table view for edits. Save a **My work** view for your own daily pass.

## Status that means something

| Status | Use it when |
| --- | --- |
| To Do | Ready, not started |
| In Progress | Someone is actively working |
| Blocked | Waiting on a decision, dependency, or external party |
| In Review | Work is complete and waiting for a check |
| Done | Accepted |
| Cancelled | Deliberately stopped |

In Review needs a named reviewer. Done means the definition of done was met.

## A few useful metrics

Metrics should change a decision. If a number never changes what you do, stop tracking it.

- **Throughput** — items finished per week. Shows whether work is closing.
- **Cycle time** — time from start to done. Shows how long work really takes.
- **Overdue count** — committed work past its date. Shows plan honesty.
- **Milestone variance** — planned versus actual milestone dates. Shows forecast quality.
- **Blocked age** — how long items sit blocked. Shows where help is missing.

Avoid vanity measures such as total tasks created or hours logged. They feel precise and say little.

## Work in progress

Limit how many items are active at once. A person with five tasks in progress has five unfinished things. Finish before starting, or say explicitly what is paused and why.

When a queue grows, find the step where work waits. That is the constraint worth fixing.

## Weekly review

Run this once a week. It is the highest-value habit in execution.

1. Open the project overview. Check progress, overdue count, and the next milestone.
2. Filter Overdue. Reschedule, finish, or cancel each item.
3. Filter Blocked. Confirm every blocker has an owner and a next action.
4. Filter Due this week. Confirm the plan is realistic.
5. Check In Review. Nudge reviewers.
6. Look at the critical path. Is anything slipping?
7. Update the brief if scope or done criteria changed.
8. Archive finished work.

## Try it

Run one weekly review on your project.

1. Clear overdue items.
2. Fix every blocked item with an owner and next action.
3. Record three metrics: throughput, overdue count, and blocked age.
4. Write one sentence on what the numbers tell you to change.

Put the review note in `local-project/pm-vault/`.

Next: [Closing](09-closing.md)
