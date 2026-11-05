# Planning and scheduling

Break the outcome into work you can estimate, order it by real constraints, and protect the dates that matter.

## Break the work down

A work breakdown structure divides the outcome until each piece is small enough to finish and estimate.

Rules that work:

- **Deliverable, not activity.** "Draft vendor comparison" is a deliverable. "Work on vendors" is not.
- **Size for feedback.** Aim for tasks that finish in one to three days.
- **Avoid duplicate work.** Two subtasks should not contain the same effort.
- **Stop at a useful depth.** Three levels is usually enough. If you need six, the top level is probably a project.

In dotpm, use tasks for major deliverables and subtasks for the breakdown. Parent progress rolls up from children.

## Estimate

An estimate is a range, not a promise. Its job is to expose uncertainty early.

Use three points when the work is uncertain:

- **Optimistic** — everything goes right.
- **Most likely** — normal friction.
- **Pessimistic** — the plausible bad case.

Expected effort is roughly `(O + 4M + P) / 6`.

Practical rules:

- Estimate in hours or half-days, not vague days.
- Add buffer at the project or phase level, not hidden inside every task.
- Break down anything you cannot estimate. That is a signal, not a failure.
- Compare estimates with actuals so the next estimate improves.

In dotpm, set `timeEstimate` on a task and log actual time as you go. The project overview shows logged versus estimated.

## Sequence

Some work must wait. Model only real constraints.

- **Dependency** — this task cannot start until another finishes.
- **Subtask** — this work is part of a larger task.
- **Milestone** — a zero-duration checkpoint such as "Vendor selected".

A dependency is not a subtask. "Write summary" is part of "Define scope" and may also depend on "Build prototype". Use each for its own purpose.

Keep dependency chains short. Long chains make every date change ripple through the plan.

## Schedule and protect

1. Set start and due dates on committed tasks.
2. Add dependencies only where the order is real.
3. Find the critical path: the longest chain of dependent work.
4. Put buffer at the end of a phase or before a major milestone.
5. Re-check the critical path when dates move.

In dotpm, the Gantt view shows bars, dependencies, and milestones. Auto-schedule moves dependents forward when dates change. If everything is urgent, the schedule is not the problem; the priorities are.

## Try it

Plan three tasks for your project.

1. Write each as a deliverable with an owner.
2. Give each an estimate and a due date.
3. Add one real dependency between them.
4. Mark one checkpoint as a milestone.
5. Add a short buffer before the milestone.

Enter this in `local-project/pm-vault/` using dotpm.

Next: [Risk and issues](05-risk-and-issues.md)
